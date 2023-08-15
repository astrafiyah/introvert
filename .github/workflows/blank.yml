-- phpMyAdmin SQL Dump
-- version 5.1.1
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1
-- Generation Time: Aug 05, 2021 at 10:51 AM
-- Server version: 10.4.20-MariaDB
-- PHP Version: 7.4.21

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `astra computer`
--
CREATE DATABASE IF NOT EXISTS `astra computer` DEFAULT CHARACTER SET utf8 COLLATE utf8_bin;
USE `astra computer`;

-- --------------------------------------------------------

--
-- Table structure for table `academic_years`
--

CREATE TABLE `academic_years` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `academic_year` varchar(9) NOT NULL COMMENT 'Tahun Pelajaran',
  `semester` enum('odd','even') NOT NULL DEFAULT 'odd' COMMENT 'odd = Ganjil, even = Genap',
  `current_semester` enum('true','false') NOT NULL DEFAULT 'false',
  `admission_semester` enum('true','false') NOT NULL DEFAULT 'false',
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `achievements`
--

CREATE TABLE `achievements` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `student_id` bigint(20) DEFAULT 0,
  `achievement_description` varchar(255) NOT NULL,
  `achievement_type` bigint(20) DEFAULT 0,
  `achievement_level` smallint(6) NOT NULL DEFAULT 0,
  `achievement_year` year(4) NOT NULL,
  `achievement_organizer` varchar(255) NOT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `admission_phases`
--

CREATE TABLE `admission_phases` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `academic_year_id` bigint(20) DEFAULT 0 COMMENT 'Tahun Pelajaran',
  `phase_name` varchar(255) NOT NULL COMMENT 'Gelombang Pendaftaran',
  `phase_start_date` date DEFAULT NULL COMMENT 'Tanggal Mulai',
  `phase_end_date` date DEFAULT NULL COMMENT 'Tanggal Selesai',
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `admission_quotas`
--

CREATE TABLE `admission_quotas` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `academic_year_id` bigint(20) DEFAULT 0 COMMENT 'Tahun Pelajaran',
  `admission_type_id` bigint(20) DEFAULT 0 COMMENT 'Jalur Pendaftaran',
  `major_id` bigint(20) DEFAULT 0 COMMENT 'Program Keahlian',
  `quota` smallint(6) NOT NULL DEFAULT 0 COMMENT 'Kuota Pendaftaran',
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `albums`
--

CREATE TABLE `albums` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `album_title` varchar(255) NOT NULL,
  `album_description` varchar(255) DEFAULT NULL,
  `album_slug` varchar(255) DEFAULT NULL,
  `album_cover` varchar(100) DEFAULT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `answers`
--

CREATE TABLE `answers` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `question_id` bigint(20) DEFAULT 0,
  `answer` varchar(255) DEFAULT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `categories`
--

CREATE TABLE `categories` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `category_name` varchar(255) NOT NULL,
  `category_slug` varchar(255) DEFAULT NULL,
  `category_description` varchar(255) DEFAULT NULL,
  `category_type` enum('post','file') DEFAULT 'post',
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `categories`
--

INSERT INTO `categories` (`id`, `category_name`, `category_slug`, `category_description`, `category_type`, `created_at`, `updated_at`, `deleted_at`, `restored_at`, `created_by`, `updated_by`, `deleted_by`, `restored_by`, `is_deleted`) VALUES
(1, 'Uncategorized', 'uncategorized', 'Uncategorized', 'post', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(2, 'Uncategorized', 'uncategorized', 'Uncategorized', 'file', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false');

-- --------------------------------------------------------

--
-- Table structure for table `class_groups`
--

CREATE TABLE `class_groups` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `class_group` varchar(100) DEFAULT NULL,
  `sub_class_group` varchar(100) DEFAULT NULL,
  `major_id` bigint(20) DEFAULT 0 COMMENT 'Program Keahlian',
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `class_group_settings`
--

CREATE TABLE `class_group_settings` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `academic_year_id` bigint(20) DEFAULT 0 COMMENT 'FK dari academic_years',
  `class_group_id` bigint(20) DEFAULT 0 COMMENT 'Kelas, FK dari class_groups',
  `employee_id` bigint(20) DEFAULT 0 COMMENT 'Wali Kelas, FK dari employees',
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `class_group_students`
--

CREATE TABLE `class_group_students` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `class_group_setting_id` bigint(20) DEFAULT 0,
  `student_id` bigint(20) DEFAULT 0,
  `is_class_manager` enum('true','false') NOT NULL DEFAULT 'false' COMMENT 'Ketua Kelas ?',
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `comments`
--

CREATE TABLE `comments` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `comment_post_id` bigint(20) DEFAULT 0,
  `comment_author` varchar(255) NOT NULL,
  `comment_email` varchar(255) DEFAULT NULL,
  `comment_url` varchar(255) DEFAULT NULL,
  `comment_ip_address` varchar(255) NOT NULL,
  `comment_content` text NOT NULL,
  `comment_subject` varchar(255) DEFAULT NULL,
  `comment_reply` text DEFAULT NULL,
  `comment_status` enum('approved','unapproved','spam') DEFAULT 'approved',
  `comment_agent` varchar(255) DEFAULT NULL,
  `comment_parent_id` varchar(255) DEFAULT NULL,
  `comment_type` enum('post','message') DEFAULT 'post',
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `employees`
--

CREATE TABLE `employees` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `assignment_letter_number` varchar(255) DEFAULT NULL COMMENT 'Nomor Surat Tugas',
  `assignment_letter_date` date DEFAULT NULL COMMENT 'Tanggal Surat Tugas',
  `assignment_start_date` date DEFAULT NULL COMMENT 'TMT Tugas',
  `parent_school_status` enum('true','false') NOT NULL DEFAULT 'true' COMMENT 'Status Sekolah Induk',
  `full_name` varchar(150) NOT NULL,
  `gender` enum('M','F') NOT NULL DEFAULT 'M',
  `nik` varchar(50) DEFAULT NULL,
  `birth_place` varchar(255) DEFAULT NULL,
  `birth_date` date DEFAULT NULL,
  `mother_name` varchar(150) DEFAULT NULL,
  `street_address` varchar(255) DEFAULT NULL COMMENT 'Alamat Jalan',
  `rt` varchar(10) DEFAULT NULL COMMENT 'Rukun Tetangga',
  `rw` varchar(10) DEFAULT NULL COMMENT 'Rukun Warga',
  `sub_village` varchar(255) DEFAULT NULL COMMENT 'Nama Dusun',
  `village` varchar(255) DEFAULT NULL COMMENT 'Nama Kelurahan/ Desa',
  `sub_district` varchar(255) DEFAULT NULL COMMENT 'Kecamatan',
  `district` varchar(255) DEFAULT NULL COMMENT 'Kabupaten',
  `postal_code` varchar(20) DEFAULT NULL COMMENT 'Kode POS',
  `religion_id` bigint(20) DEFAULT 0,
  `marriage_status_id` bigint(20) DEFAULT 0,
  `spouse_name` varchar(255) DEFAULT NULL COMMENT 'Nama Pasangan : Suami / Istri',
  `spouse_employment_id` bigint(20) DEFAULT 0 COMMENT 'Pekerjaan Pasangan : Suami / Istri',
  `citizenship` enum('WNI','WNA') NOT NULL DEFAULT 'WNI' COMMENT 'Kewarganegaraan',
  `country` varchar(255) DEFAULT NULL,
  `npwp` varchar(100) DEFAULT NULL,
  `employment_status_id` bigint(20) DEFAULT 0 COMMENT 'Status Kepegawaian',
  `nip` varchar(100) DEFAULT NULL,
  `niy` varchar(100) DEFAULT NULL COMMENT 'NIY/NIGK',
  `nuptk` varchar(100) DEFAULT NULL,
  `employment_type_id` bigint(20) DEFAULT 0 COMMENT 'Jenis Guru dan Tenaga Kependidikan (GTK)',
  `decree_appointment` varchar(255) DEFAULT NULL COMMENT 'SK Pengangkatan',
  `appointment_start_date` date DEFAULT NULL COMMENT 'TMT Pengangkatan',
  `institution_lifter_id` bigint(20) DEFAULT 0 COMMENT 'Lembaga Pengangkat',
  `decree_cpns` varchar(100) DEFAULT NULL COMMENT 'SK CPNS',
  `pns_start_date` date DEFAULT NULL COMMENT 'TMT CPNS',
  `rank_id` bigint(20) DEFAULT 0 COMMENT 'Pangkat / Golongan',
  `salary_source_id` bigint(20) DEFAULT 0 COMMENT 'Sumber Gaji',
  `headmaster_license` enum('true','false') NOT NULL DEFAULT 'false' COMMENT 'Punya Lisensi Kepala Sekolah ?',
  `laboratory_skill_id` bigint(20) DEFAULT 0 COMMENT 'Keahlian Lab oratorium',
  `special_need_id` bigint(20) DEFAULT 0 COMMENT 'Mampu Menangani Kebutuhan Khusus',
  `braille_skills` enum('true','false') NOT NULL DEFAULT 'false' COMMENT 'Keahlian Braile ?',
  `sign_language_skills` enum('true','false') NOT NULL DEFAULT 'false' COMMENT 'Keahlian Bahasa Isyarat ?',
  `phone` varchar(255) DEFAULT NULL,
  `mobile_phone` varchar(255) DEFAULT NULL,
  `email` varchar(255) DEFAULT NULL,
  `photo` varchar(100) DEFAULT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `files`
--

CREATE TABLE `files` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `file_title` varchar(255) DEFAULT NULL,
  `file_description` varchar(255) DEFAULT NULL,
  `file_name` varchar(255) DEFAULT NULL,
  `file_type` varchar(255) DEFAULT NULL,
  `file_category_id` bigint(20) DEFAULT 0,
  `file_path` varchar(255) DEFAULT NULL,
  `file_ext` varchar(255) DEFAULT NULL,
  `file_size` varchar(255) DEFAULT NULL,
  `file_visibility` enum('public','private') DEFAULT 'public',
  `file_counter` bigint(20) DEFAULT 0,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `image_sliders`
--

CREATE TABLE `image_sliders` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `caption` varchar(255) NOT NULL,
  `image` varchar(255) DEFAULT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `image_sliders`
--

INSERT INTO `image_sliders` (`id`, `caption`, `image`, `created_at`, `updated_at`, `deleted_at`, `restored_at`, `created_by`, `updated_by`, `deleted_by`, `restored_by`, `is_deleted`) VALUES
(1, 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua', '1.png', '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(2, 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua', '2.png', '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false');

-- --------------------------------------------------------

--
-- Table structure for table `links`
--

CREATE TABLE `links` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `link_title` varchar(255) NOT NULL,
  `link_url` varchar(255) DEFAULT NULL,
  `link_target` enum('_blank','_self','_parent','_top') DEFAULT '_blank',
  `link_image` varchar(100) DEFAULT NULL,
  `link_type` enum('link','banner') DEFAULT 'link',
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `links`
--

INSERT INTO `links` (`id`, `link_title`, `link_url`, `link_target`, `link_image`, `link_type`, `created_at`, `updated_at`, `deleted_at`, `restored_at`, `created_by`, `updated_by`, `deleted_by`, `restored_by`, `is_deleted`) VALUES
(1, 'CMS Computer', 'https://linktr.ee/misda_masda', '_blank', NULL, 'link', '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(2, 'CMS Computer', 'https://linktr.ee/misda_masda', '_blank', '1.png', 'banner', '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false');

-- --------------------------------------------------------

--
-- Table structure for table `login_attempts`
--

CREATE TABLE `login_attempts` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `ip_address` varchar(45) NOT NULL,
  `counter` int(11) UNSIGNED NOT NULL DEFAULT 1,
  `datetime` datetime DEFAULT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `majors`
--

CREATE TABLE `majors` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `major_name` varchar(255) DEFAULT NULL COMMENT 'Program Keahlian / Jurusan',
  `major_short_name` varchar(255) DEFAULT NULL COMMENT 'Nama Singkat',
  `is_active` enum('true','false') DEFAULT 'true',
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `menus`
--

CREATE TABLE `menus` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `menu_title` varchar(150) NOT NULL,
  `menu_url` varchar(150) NOT NULL,
  `menu_target` enum('_blank','_self','_parent','_top') DEFAULT '_self',
  `menu_type` varchar(100) NOT NULL DEFAULT 'pages',
  `menu_parent_id` bigint(20) DEFAULT 0,
  `menu_position` bigint(20) DEFAULT 0,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `menus`
--

INSERT INTO `menus` (`id`, `menu_title`, `menu_url`, `menu_target`, `menu_type`, `menu_parent_id`, `menu_position`, `created_at`, `updated_at`, `deleted_at`, `restored_at`, `created_by`, `updated_by`, `deleted_by`, `restored_by`, `is_deleted`) VALUES
(1, 'Hubungi Kami', 'hubungi-kami', '_self', 'modules', 0, 7, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(2, 'Galeri Foto', 'galeri-foto', '_self', 'modules', 9, 1, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(3, 'Galeri Video', 'galeri-video', '_self', 'modules', 9, 2, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(4, 'Formulir PPDB', 'formulir-penerimaan-peserta-didik-baru', '_self', 'modules', 8, 1, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(5, 'Hasil Seleksi', 'hasil-seleksi-penerimaan-peserta-didik-baru', '_self', 'modules', 8, 2, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(6, 'Cetak Formulir', 'cetak-formulir-penerimaan-peserta-didik-baru', '_self', 'modules', 8, 3, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(7, 'Download Formulir', 'download-formulir-penerimaan-peserta-didik-baru', '_self', 'modules', 8, 4, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(8, 'PPDB 2019', '#', '_self', 'links', 0, 5, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(9, 'Galeri', '#', '_self', 'links', 0, 6, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(10, 'Kategori', '#', '_self', 'links', 0, 2, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(11, 'Uncategorized', 'kategori/uncategorized', '_self', 'post_categories', 10, 1, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(12, 'Direktori', '#', '_self', 'links', 0, 3, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(13, 'Direktori Alumni', 'direktori-alumni', '_self', 'modules', 12, 1, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(14, 'Direktori Peserta Didik', 'direktori-peserta-didik', '_self', 'modules', 12, 3, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(15, 'Direktori Guru dan Tenaga Kependidikan', 'direktori-guru-dan-tenaga-kependidikan', '_self', 'modules', 12, 2, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(16, 'Pendaftaran Alumni', 'pendaftaran-alumni', '_self', 'modules', 0, 4, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(17, 'Profil', 'read/2/profil', '_self', 'pages', 0, 1, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(18, 'Visi dan Misi', 'read/3/visi-dan-misi', '_self', 'pages', 0, 1, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false');

-- --------------------------------------------------------

--
-- Table structure for table `modules`
--

CREATE TABLE `modules` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `module_name` varchar(255) NOT NULL,
  `module_description` varchar(255) DEFAULT NULL,
  `module_url` varchar(255) DEFAULT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `modules`
--

INSERT INTO `modules` (`id`, `module_name`, `module_description`, `module_url`, `created_at`, `updated_at`, `deleted_at`, `restored_at`, `created_by`, `updated_by`, `deleted_by`, `restored_by`, `is_deleted`) VALUES
(1, 'Pengguna', 'Pengguna', 'users', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(2, 'PPDB / PMB', 'PPDB / PMB', 'admission', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(3, 'Tampilan', 'Tampilan', 'appearance', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(4, 'Blog', 'Blog', 'blog', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(5, 'GTK / Staff / Dosen', 'GTK / Staff / Dosen', 'employees', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(6, 'Media', 'Media', 'media', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(7, 'Plugins', 'Plugins', 'plugins', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(8, 'Data Referensi', 'Data Referensi', 'reference', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(9, 'Pengaturan', 'Pengaturan', 'settings', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(10, 'Akademik', 'Akademik', 'academic', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false');

-- --------------------------------------------------------

--
-- Table structure for table `options`
--

CREATE TABLE `options` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `option_group` varchar(100) NOT NULL,
  `option_name` varchar(255) DEFAULT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `options`
--

INSERT INTO `options` (`id`, `option_group`, `option_name`, `created_at`, `updated_at`, `deleted_at`, `restored_at`, `created_by`, `updated_by`, `deleted_by`, `restored_by`, `is_deleted`) VALUES
(1, 'student_status', 'Aktif', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(2, 'student_status', 'Lulus', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(3, 'student_status', 'Mutasi', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(4, 'student_status', 'Dikeluarkan', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(5, 'student_status', 'Mengundurkan Diri', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(6, 'student_status', 'Putus Sekolah', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(7, 'student_status', 'Meninggal', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(8, 'student_status', 'Hilang', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(9, 'student_status', 'Lainnya', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(10, 'employments', 'Tidak bekerja', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(11, 'employments', 'Nelayan', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(12, 'employments', 'Petani', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(13, 'employments', 'Peternak', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(14, 'employments', 'PNS/TNI/POLRI', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(15, 'employments', 'Karyawan Swasta', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(16, 'employments', 'Pedagang Kecil', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(17, 'employments', 'Pedagang Besar', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(18, 'employments', 'Wiraswasta', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(19, 'employments', 'Wirausaha', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(20, 'employments', 'Buruh', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(21, 'employments', 'Pensiunan', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(22, 'employments', 'Lain-lain', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(23, 'special_needs', 'Tidak', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(24, 'special_needs', 'Tuna Netra', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(25, 'special_needs', 'Tuna Rungu', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(26, 'special_needs', 'Tuna Grahita ringan', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(27, 'special_needs', 'Tuna Grahita Sedang', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(28, 'special_needs', 'Tuna Daksa Ringan', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(29, 'special_needs', 'Tuna Daksa Sedang', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(30, 'special_needs', 'Tuna Laras', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(31, 'special_needs', 'Tuna Wicara', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(32, 'special_needs', 'Tuna ganda', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(33, 'special_needs', 'Hiper aktif', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(34, 'special_needs', 'Cerdas Istimewa', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(35, 'special_needs', 'Bakat Istimewa', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(36, 'special_needs', 'Kesulitan Belajar', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(37, 'special_needs', 'Narkoba', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(38, 'special_needs', 'Indigo', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(39, 'special_needs', 'Down Sindrome', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(40, 'special_needs', 'Autis', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(41, 'special_needs', 'Lainnya', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(42, 'educations', 'Tidak sekolah', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(43, 'educations', 'Putus SD', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(44, 'educations', 'SD Sederajat', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(45, 'educations', 'SMP Sederajat', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(46, 'educations', 'SMA Sederajat', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(47, 'educations', 'D1', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(48, 'educations', 'D2', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(49, 'educations', 'D3', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(50, 'educations', 'D4/S1', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(51, 'educations', 'S2', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(52, 'educations', 'S3', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(53, 'scholarships', 'Anak berprestasi', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(54, 'scholarships', 'Anak Miskin', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(55, 'scholarships', 'Pendidikan', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(56, 'scholarships', 'Unggulan', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(57, 'scholarships', 'Lain-lain', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(58, 'achievement_types', 'Sains', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(59, 'achievement_types', 'Seni', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(60, 'achievement_types', 'Olahraga', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(61, 'achievement_types', 'Lain-lain', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(62, 'achievement_levels', 'Sekolah', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(63, 'achievement_levels', 'Kecamatan', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(64, 'achievement_levels', 'Kabupaten', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(65, 'achievement_levels', 'Provinsi', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(66, 'achievement_levels', 'Nasional', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(67, 'achievement_levels', 'Internasional', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(68, 'monthly_incomes', 'Kurang dari 500,000', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(69, 'monthly_incomes', '500.000 - 999.9999', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(70, 'monthly_incomes', '1 Juta - 1.999.999', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(71, 'monthly_incomes', '2 Juta - 4.999.999', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(72, 'monthly_incomes', '5 Juta - 20 Juta', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(73, 'monthly_incomes', 'Lebih dari 20 Juta', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(74, 'residences', 'Bersama orang tua', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(75, 'residences', 'Wali', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(76, 'residences', 'Kos', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(77, 'residences', 'Asrama', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(78, 'residences', 'Panti Asuhan', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(79, 'residences', 'Lainnya', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(80, 'transportations', 'Jalan kaki', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(81, 'transportations', 'Kendaraan pribadi', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(82, 'transportations', 'Kendaraan Umum / angkot / Pete-pete', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(83, 'transportations', 'Jemputan Sekolah', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(84, 'transportations', 'Kereta Api', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(85, 'transportations', 'Ojek', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(86, 'transportations', 'Andong / Bendi / Sado / Dokar / Delman / Beca', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(87, 'transportations', 'Perahu penyebrangan / Rakit / Getek', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(88, 'transportations', 'Lainnya', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(89, 'religions', 'Islam', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(90, 'religions', 'Kristen / protestan', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(91, 'religions', 'Katholik', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(92, 'religions', 'Hindu', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(93, 'religions', 'Budha', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(94, 'religions', 'Khong Hu Chu', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(95, 'religions', 'Lainnya', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(96, 'school_levels', '1 - Sekolah Dasar (SD) / Sederajat', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(97, 'school_levels', '2 - Sekolah Menengah Pertama (SMP) / Sederajat', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(98, 'school_levels', '3 - Sekolah Menengah Atas (SMA) / Aliyah', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(99, 'school_levels', '4 - Sekolah Menengah Kejuruan (SMK)', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(100, 'school_levels', '5 - Universitas', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(101, 'school_levels', '6 - Sekolah Tinggi', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(102, 'school_levels', '7 - Politeknik', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(103, 'marriage_status', 'Kawin', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(104, 'marriage_status', 'Belum Kawin', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(105, 'marriage_status', 'Berpisah', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(106, 'institution_lifters', 'Pemerintah Pusat', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(107, 'institution_lifters', 'Pemerintah Provinsi', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(108, 'institution_lifters', 'Pemerintah Kab/Kota', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(109, 'institution_lifters', 'Ketua yayasan', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(110, 'institution_lifters', 'Kepala Sekolah', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(111, 'institution_lifters', 'Komite Sekolah', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(112, 'institution_lifters', 'Lainnya', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(113, 'employment_status', 'PNS ', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(114, 'employment_status', 'PNS Diperbantukan ', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(115, 'employment_status', 'PNS DEPAG ', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(116, 'employment_status', 'GTY/PTY ', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(117, 'employment_status', 'GTT/PTT Provinsi ', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(118, 'employment_status', 'GTT/PTT Kabupaten/Kota', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(119, 'employment_status', 'Guru Bantu Pusat ', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(120, 'employment_status', 'Guru Honor Sekolah ', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(121, 'employment_status', 'Tenaga Honor Sekolah ', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(122, 'employment_status', 'CPNS', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(123, 'employment_status', 'Lainnya', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(124, 'employment_types', 'Guru Kelas', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(125, 'employment_types', 'Guru Mata Pelajaran', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(126, 'employment_types', 'Guru BK', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(127, 'employment_types', 'Guru Inklusi', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(128, 'employment_types', 'Tenaga Administrasi Sekolah', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(129, 'employment_types', 'Guru Pendamping', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(130, 'employment_types', 'Guru Magang', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(131, 'employment_types', 'Guru TIK', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(132, 'employment_types', 'Laboran', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(133, 'employment_types', 'Pustakawan', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(134, 'employment_types', 'Lainnya', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(135, 'ranks', 'I/A', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(136, 'ranks', 'I/B', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(137, 'ranks', 'I/C', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(138, 'ranks', 'I/D', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(139, 'ranks', 'II/A', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(140, 'ranks', 'II/B', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(141, 'ranks', 'II/C', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(142, 'ranks', 'II/D', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(143, 'ranks', 'III/A', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(144, 'ranks', 'III/B', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(145, 'ranks', 'III/C', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(146, 'ranks', 'III/D', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(147, 'ranks', 'IV/A', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(148, 'ranks', 'IV/B', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(149, 'ranks', 'IV/C', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(150, 'ranks', 'IV/D', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(151, 'ranks', 'IV/E', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(152, 'salary_sources', 'APBN', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(153, 'salary_sources', 'APBD Provinsi', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(154, 'salary_sources', 'APBD Kab/Kota', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(155, 'salary_sources', 'Yayasan', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(156, 'salary_sources', 'Sekolah', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(157, 'salary_sources', 'Lembaga Donor', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(158, 'salary_sources', 'Lainnya', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(159, 'laboratory_skills', 'Lab IPA', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(160, 'laboratory_skills', 'Lab Fisika', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(161, 'laboratory_skills', 'Lab Biologi', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(162, 'laboratory_skills', 'Lab Kimia', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(163, 'laboratory_skills', 'Lab Bahasa', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(164, 'laboratory_skills', 'Lab Komputer', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(165, 'laboratory_skills', 'Teknik Bangunan', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(166, 'laboratory_skills', 'Teknik Survei & Pemetaan', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(167, 'laboratory_skills', 'Teknik Ketenagakerjaan', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(168, 'laboratory_skills', 'Teknik Pendinginan & Tata Udara', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(169, 'laboratory_skills', 'Teknik Mesin', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false');

-- --------------------------------------------------------

--
-- Table structure for table `photos`
--

CREATE TABLE `photos` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `photo_album_id` bigint(20) DEFAULT 0,
  `photo_name` varchar(255) NOT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `pollings`
--

CREATE TABLE `pollings` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `answer_id` bigint(20) DEFAULT 0,
  `ip_address` varchar(45) DEFAULT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `posts`
--

CREATE TABLE `posts` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `post_title` varchar(255) DEFAULT NULL,
  `post_content` longtext DEFAULT NULL,
  `post_image` varchar(100) DEFAULT NULL,
  `post_author` bigint(20) DEFAULT 0,
  `post_categories` varchar(255) DEFAULT NULL,
  `post_type` varchar(50) NOT NULL DEFAULT 'post',
  `post_status` enum('publish','draft') DEFAULT 'draft',
  `post_visibility` enum('public','private') DEFAULT 'public',
  `post_comment_status` enum('open','close') DEFAULT 'close',
  `post_slug` varchar(255) DEFAULT NULL,
  `post_tags` varchar(255) DEFAULT NULL,
  `post_counter` bigint(20) DEFAULT 0,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `posts`
--

INSERT INTO `posts` (`id`, `post_title`, `post_content`, `post_image`, `post_author`, `post_categories`, `post_type`, `post_status`, `post_visibility`, `post_comment_status`, `post_slug`, `post_tags`, `post_counter`, `created_at`, `updated_at`, `deleted_at`, `restored_at`, `created_by`, `updated_by`, `deleted_by`, `restored_by`, `is_deleted`) VALUES
(1, '', '<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>', 'headmaster_photo.png', 0, '', 'opening_speech', 'publish', 'public', 'open', '', '', 0, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(2, 'Profil', '<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>', NULL, 1, '+1+', 'page', 'publish', 'public', 'open', 'profil', 'berita, pengumuman, sekilas-info', 1, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(3, 'Visi dan Misi', '<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>', NULL, 1, '+1+', 'page', 'publish', 'public', 'open', 'visi-dan-misi', 'berita, pengumuman, sekilas-info', 1, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(4, 'Sample Post 1', '<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>', 'post_image.png', 1, '+1+', 'post', 'publish', 'public', 'open', 'sample-post-1', 'berita, pengumuman, sekilas-info', 5, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(5, 'Sample Post 2', '<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>', 'post_image.png', 1, '+1+', 'post', 'publish', 'public', 'open', 'sample-post-2', 'berita, pengumuman, sekilas-info', 1, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(6, 'Sample Post 3', '<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>', 'post_image.png', 1, '+1+', 'post', 'publish', 'public', 'open', 'sample-post-3', 'berita, pengumuman, sekilas-info', 1, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(7, 'Sample Post 4', '<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>', 'post_image.png', 1, '+1+', 'post', 'publish', 'public', 'open', 'sample-post-4', 'berita, pengumuman, sekilas-info', 1, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false'),
(8, 'Sample Post 5', '<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>', 'post_image.png', 1, '+1+', 'post', 'publish', 'public', 'open', 'sample-post-5', 'berita, pengumuman, sekilas-info', 1, '2019-09-14 08:57:43', '2019-09-14 01:57:43', NULL, NULL, 0, 0, 0, 0, 'false');

-- --------------------------------------------------------

--
-- Table structure for table `questions`
--

CREATE TABLE `questions` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `question` varchar(255) DEFAULT NULL,
  `is_active` enum('true','false') DEFAULT 'false',
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `quotes`
--

CREATE TABLE `quotes` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `quote` varchar(255) DEFAULT NULL,
  `quote_by` varchar(255) DEFAULT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `quotes`
--

INSERT INTO `quotes` (`id`, `quote`, `quote_by`, `created_at`, `updated_at`, `deleted_at`, `restored_at`, `created_by`, `updated_by`, `deleted_by`, `restored_by`, `is_deleted`) VALUES
(1, 'Pendidikan merupakan tiket untuk masa depan. Hari esok untuk orang-orang yang telah mempersiapkan dirinya hari ini', 'Anonim', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 1, 0, 0, 0, 'false'),
(2, 'Agama tanpa ilmu pengetahuan adalah buta. Dan ilmu pengetahuan tanpa agama adalah lumpuh', 'Anonim', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 1, 0, 0, 0, 'false'),
(3, 'Hiduplah seakan-akan kau akan mati besok. Belajarlah seakan-akan kau akan hidup selamanya', 'Anonim', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 1, 0, 0, 0, 'false');

-- --------------------------------------------------------

--
-- Table structure for table `scholarships`
--

CREATE TABLE `scholarships` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `student_id` bigint(20) DEFAULT 0,
  `scholarship_type` bigint(20) DEFAULT 0,
  `scholarship_description` varchar(255) NOT NULL,
  `scholarship_start_year` year(4) NOT NULL,
  `scholarship_end_year` year(4) NOT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `settings`
--

CREATE TABLE `settings` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `setting_group` varchar(100) NOT NULL,
  `setting_variable` varchar(255) DEFAULT NULL,
  `setting_value` text DEFAULT NULL,
  `setting_default_value` text DEFAULT NULL,
  `setting_access_group` varchar(255) DEFAULT NULL,
  `setting_description` varchar(255) DEFAULT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `settings`
--

INSERT INTO `settings` (`id`, `setting_group`, `setting_variable`, `setting_value`, `setting_default_value`, `setting_access_group`, `setting_description`, `created_at`, `updated_at`, `deleted_at`, `restored_at`, `created_by`, `updated_by`, `deleted_by`, `restored_by`, `is_deleted`) VALUES
(1, 'general', 'site_maintenance', NULL, 'false', 'public', 'Pemeliharaan situs', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(2, 'general', 'site_maintenance_end_date', NULL, '2019-01-01', 'public', 'Tanggal Berakhir Pemeliharaan Situs', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(3, 'general', 'site_cache', NULL, 'false', 'public', 'Cache situs', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(4, 'general', 'site_cache_time', NULL, '10', 'public', 'Lama Cache Situs', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(5, 'general', 'meta_description', NULL, 'CMS Sekolahku adalah Content Management System dan PPDB Online gratis untuk SD SMP/Sederajat SMA/Sederajat', 'public', 'Deskripsi Meta', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(6, 'general', 'meta_keywords', NULL, 'CMS, Website Sekolah Gratis, Cara Membuat Website Sekolah, membuat web sekolah, contoh website sekolah, fitur website sekolah, Sekolah, Website, Internet,Situs, CMS Sekolah, Web Sekolah, Website Sekolah Gratis, Website Sekolah, Aplikasi Sekolah, PPDB Online, PSB Online, PSB Online Gratis, Penerimaan Siswa Baru Online, Raport Online, Kurikulum 2013, SD, SMP, SMA, Aliyah, MTs, SMK', 'public', 'Kata Kunci Meta', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(7, 'general', 'map_location', NULL, '', 'public', 'Lokasi di Google Maps', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(8, 'general', 'favicon', NULL, 'favicon.png', 'public', 'Favicon', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(9, 'general', 'header', NULL, 'header.png', 'public', 'Gambar Header', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(10, 'general', 'recaptcha_status', NULL, 'disable', 'public', 'reCAPTCHA Status', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(11, 'general', 'recaptcha_site_key', NULL, '6LeNCTAUAAAAAADTbL1rDw8GT1DF2DUjVtEXzdMu', 'public', 'Recaptcha Site Key', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(12, 'general', 'recaptcha_secret_key', NULL, '6LeNCTAUAAAAAGq8O0ItkzG8fsA9KeJ7mFMMFF1s', 'public', 'Recaptcha Secret Key', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(13, 'general', 'timezone', NULL, 'Asia/Jakarta', 'public', 'Time Zone', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(14, 'media', 'file_allowed_types', NULL, 'jpg, jpeg, png, gif', 'public', 'Tipe file yang diizinkan', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(15, 'media', 'upload_max_filesize', NULL, '0', 'public', 'Maksimal Ukuran File yang Diupload', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(16, 'media', 'thumbnail_size_height', NULL, '100', 'public', 'Tinggi Gambar Thumbnail', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(17, 'media', 'thumbnail_size_width', NULL, '150', 'public', 'Lebar Gambar Thumbnail', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(18, 'media', 'medium_size_height', NULL, '308', 'public', 'Tinggi Gambar Sedang', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(19, 'media', 'medium_size_width', NULL, '460', 'public', 'Lebar Gambar Sedang', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(20, 'media', 'large_size_height', NULL, '600', 'public', 'Tinggi Gambar Besar', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(21, 'media', 'large_size_width', NULL, '800', 'public', 'Lebar Gambar Besar', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(22, 'media', 'album_cover_height', NULL, '250', 'public', 'Tinggi Cover Album Foto', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(23, 'media', 'album_cover_width', NULL, '400', 'public', 'Lebar Cover Album Foto', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(24, 'media', 'banner_height', NULL, '81', 'public', 'Tinggi Iklan', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(25, 'media', 'banner_width', NULL, '245', 'public', 'Lebar Iklan', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(26, 'media', 'image_slider_height', NULL, '400', 'public', 'Tinggi Gambar Slide', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(27, 'media', 'image_slider_width', NULL, '900', 'public', 'Lebar Gambar Slide', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(28, 'media', 'student_photo_height', NULL, '400', 'public', 'Tinggi Photo Peserta Didik', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(29, 'media', 'student_photo_width', NULL, '300', 'public', 'Lebar Photo Peserta Didik', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(30, 'media', 'employee_photo_height', NULL, '400', 'public', 'Tinggi Photo Guru dan Tenaga Kependidikan', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(31, 'media', 'employee_photo_width', NULL, '300', 'public', 'Lebar Photo Guru dan Tenaga Kependidikan', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(32, 'media', 'headmaster_photo_height', NULL, '400', 'public', 'Tinggi Photo Kepala Sekolah', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(33, 'media', 'headmaster_photo_width', NULL, '300', 'public', 'Lebar Photo Kepala Sekolah', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(34, 'media', 'header_height', NULL, '80', 'public', 'Tinggi Gambar Header', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(35, 'media', 'header_width', NULL, '200', 'public', 'Lebar Gambar Header', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(36, 'media', 'logo_height', NULL, '120', 'public', 'Tinggi Logo Sekolah', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(37, 'media', 'logo_width', NULL, '120', 'public', 'Lebar Logo Sekolah', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(38, 'writing', 'default_post_category', NULL, '1', 'public', 'Default Kategori Tulisan', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(39, 'writing', 'default_post_status', NULL, 'publish', 'public', 'Default Status Tulisan', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(40, 'writing', 'default_post_visibility', NULL, 'public', 'public', 'Default Akses Tulisan', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(41, 'writing', 'default_post_discussion', NULL, 'open', 'public', 'Default Komentar Tulisan', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(42, 'writing', 'post_image_thumbnail_height', NULL, '100', 'public', 'Tinggi Gambar Kecil', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(43, 'writing', 'post_image_thumbnail_width', NULL, '150', 'public', 'Lebar Gambar Kecil', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(44, 'writing', 'post_image_medium_height', NULL, '250', 'public', 'Tinggi Gambar Sedang', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(45, 'writing', 'post_image_medium_width', NULL, '400', 'public', 'Lebar Gambar Sedang', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(46, 'writing', 'post_image_large_height', NULL, '450', 'public', 'Tinggi Gambar Besar', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(47, 'writing', 'post_image_large_width', NULL, '840', 'public', 'Lebar Gambar Besar', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(48, 'reading', 'post_per_page', NULL, '10', 'public', 'Tulisan per halaman', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(49, 'reading', 'post_rss_count', NULL, '10', 'public', 'Jumlah RSS', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(50, 'reading', 'post_related_count', NULL, '10', 'public', 'Jumlah Tulisan Terkait', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(51, 'reading', 'comment_per_page', NULL, '10', 'public', 'Komentar per halaman', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(52, 'discussion', 'comment_moderation', NULL, 'false', 'public', 'Komentar harus disetujui secara manual', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(53, 'discussion', 'comment_registration', NULL, 'false', 'public', 'Pengguna harus terdaftar dan login untuk komentar', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(54, 'discussion', 'comment_blacklist', NULL, 'kampret', 'public', 'Komentar disaring', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(55, 'discussion', 'comment_order', NULL, 'asc', 'public', 'Urutan Komentar', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(56, 'social_account', 'facebook', NULL, '', 'public', 'Facebook', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(57, 'social_account', 'twitter', NULL, '', 'public', 'Twitter', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(58, 'social_account', 'linked_in', NULL, '', 'public', 'Linked In', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(59, 'social_account', 'youtube', NULL, '', 'public', 'Youtube', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(60, 'social_account', 'instagram', NULL, '', 'public', 'Instagram', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(61, 'mail_server', 'sendgrid_username', NULL, '', 'public', 'Sendgrid Username', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(62, 'mail_server', 'sendgrid_password', NULL, '', 'public', 'Sendgrid Password', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(63, 'mail_server', 'sendgrid_api_key', NULL, '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', 'public', 'Sendgrid API Key', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(64, 'school_profile', 'npsn', NULL, '123', 'public', 'NPSN', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(65, 'school_profile', 'school_name', NULL, 'SMA Negeri 9 Kuningan', 'public', 'Nama Sekolah', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(66, 'school_profile', 'headmaster', NULL, 'Anton Sofyan', 'public', 'Kepala Sekolah', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(67, 'school_profile', 'headmaster_photo', NULL, 'headmaster_photo.png', 'public', 'Photo Kepala Sekolah', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(68, 'school_profile', 'school_level', NULL, '3', 'public', 'Bentuk Pendidikan', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(69, 'school_profile', 'school_status', NULL, '1', 'public', 'Status Sekolah', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(70, 'school_profile', 'ownership_status', NULL, '1', 'public', 'Status Kepemilikan', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(71, 'school_profile', 'decree_operating_permit', NULL, '-', 'public', 'SK Izin Operasional', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(72, 'school_profile', 'decree_operating_permit_date', NULL, '2019-09-14', 'public', 'Tanggal SK Izin Operasional', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(73, 'school_profile', 'tagline', NULL, 'Where Tomorrow\'s Leaders Come Together', 'public', 'Slogan', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(74, 'school_profile', 'rt', NULL, '12', 'public', 'RT', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(75, 'school_profile', 'rw', NULL, '06', 'public', 'RW', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(76, 'school_profile', 'sub_village', NULL, 'Geneng Indah', 'public', 'Dusun', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(77, 'school_profile', 'village', NULL, 'Deket Kulon', 'public', 'Kelurahan / Desa', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(78, 'school_profile', 'sub_district', NULL, 'Deket', 'public', 'Kecamatan', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(79, 'school_profile', 'district', NULL, 'Lamongan', 'public', 'Kabupaten', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(80, 'school_profile', 'postal_code', NULL, '62291', 'public', 'Kode Pos', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(81, 'school_profile', 'street_address', NULL, 'Jalan Panglima Sudirman No. 221', 'public', 'Alamat Jalan', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(82, 'school_profile', 'phone', NULL, '+6285607280212', 'public', 'Telepon', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(83, 'school_profile', 'handphone', NULL, '+6285642469291', 'public', 'Fax', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(84, 'school_profile', 'email', NULL, 'misdafatma@outlook.com', 'public', 'Email', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(85, 'school_profile', 'website', NULL, 'http://www.linktr.ee/misda_masda', 'public', 'Website', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(86, 'school_profile', 'logo', NULL, 'logo.png', 'public', 'Logo', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(87, 'admission', 'admission_status', NULL, 'open', 'public', 'Status Penerimaan Peserta Didik Baru', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(88, 'admission', 'admission_year', NULL, '2019', 'public', 'Tahun Penerimaan Peserta Didik Baru', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(89, 'admission', 'admission_start_date', NULL, '2019-01-01', 'public', 'Tanggal Mulai PPDB', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(90, 'admission', 'admission_end_date', NULL, '2019-12-31', 'public', 'Tanggal Selesai PPDB', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(91, 'admission', 'announcement_start_date', NULL, '2019-01-01', 'public', 'Tanggal Mulai Pengumuman Hasil Seleksi PPDB', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false'),
(92, 'admission', 'announcement_end_date', NULL, '2019-12-31', 'public', 'Tanggal Selesai Pengumuman Hasil Seleksi PPDB', '2019-09-14 08:57:41', '2019-09-14 01:57:41', NULL, NULL, 0, 0, 0, 0, 'false');

-- --------------------------------------------------------

--
-- Table structure for table `students`
--

CREATE TABLE `students` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `major_id` bigint(20) DEFAULT 0 COMMENT 'Program Keahlian',
  `first_choice_id` bigint(20) DEFAULT 0 COMMENT 'Pilihan Pertama PPDB',
  `second_choice_id` bigint(20) DEFAULT 0 COMMENT 'Pilihan Kedua PPDB',
  `registration_number` varchar(10) DEFAULT NULL COMMENT 'Nomor Pendaftaran',
  `admission_exam_number` varchar(10) DEFAULT NULL COMMENT 'Nomor Ujian Tes Tulis',
  `selection_result` varchar(100) DEFAULT NULL COMMENT 'Hasil Seleksi PPDB/PMB',
  `admission_phase_id` bigint(20) DEFAULT 0 COMMENT 'Gelombang Pendaftaran',
  `admission_type_id` bigint(20) DEFAULT 0 COMMENT 'Jalur Pendaftaran',
  `photo` varchar(100) DEFAULT NULL,
  `achievement` text DEFAULT NULL COMMENT 'Prestasi Calon Peserta Didik / Mahasiswa',
  `is_student` enum('true','false') NOT NULL DEFAULT 'false' COMMENT 'Apakah Siswa Aktif ? Set true jika lolos seleksi PPDB dan set FALSE jika sudah lulus',
  `is_prospective_student` enum('true','false') NOT NULL DEFAULT 'false' COMMENT 'Apakah Calon Siswa Baru ?',
  `is_alumni` enum('true','false','unverified') NOT NULL DEFAULT 'false' COMMENT 'Apakah Alumni ?',
  `is_transfer` enum('true','false') NOT NULL DEFAULT 'false' COMMENT 'Jenis Pendaftaran : Baru / Pindahan ?',
  `re_registration` enum('true','false') DEFAULT NULL COMMENT 'Konfirmasi Pendaftaran Ulang Calon Siswa Baru',
  `start_date` date DEFAULT NULL COMMENT 'Tanggal Masuk Sekolah',
  `identity_number` varchar(50) DEFAULT NULL COMMENT 'NIS/NIM',
  `nisn` varchar(50) DEFAULT NULL COMMENT 'Nomor Induk Siswa Nasional',
  `nik` varchar(50) DEFAULT NULL COMMENT 'Nomor Induk Kependudukan / KTP',
  `prev_exam_number` varchar(50) DEFAULT NULL COMMENT 'Nomor Peserta Ujian Sebelumnya',
  `prev_diploma_number` varchar(50) DEFAULT NULL COMMENT 'Nomor Ijazah Sebelumnya',
  `paud` enum('true','false') DEFAULT NULL COMMENT 'Apakah pernah PAUD',
  `tk` enum('true','false') DEFAULT NULL COMMENT 'Apakah pernah TK',
  `skhun` varchar(50) DEFAULT NULL COMMENT 'No. Seri Surat Keterangan Hasil Ujian Nasional Sebelumnya',
  `prev_school_name` varchar(255) DEFAULT NULL COMMENT 'Nama Sekolah Sebelumnya',
  `prev_school_address` varchar(255) DEFAULT NULL COMMENT 'Alamat Sekolah Sebelumnya',
  `hobby` varchar(255) DEFAULT NULL,
  `ambition` varchar(255) DEFAULT NULL COMMENT 'Cita-cita',
  `full_name` varchar(150) NOT NULL,
  `gender` enum('M','F') NOT NULL DEFAULT 'M',
  `birth_place` varchar(255) DEFAULT NULL,
  `birth_date` date DEFAULT NULL,
  `religion_id` bigint(20) DEFAULT 0,
  `special_need_id` bigint(20) DEFAULT 0 COMMENT 'Berkeburuhan Khusus',
  `street_address` varchar(255) DEFAULT NULL COMMENT 'Alamat Jalan',
  `rt` varchar(10) DEFAULT NULL COMMENT 'Alamat Jalan',
  `rw` varchar(10) DEFAULT NULL COMMENT 'Alamat Jalan',
  `sub_village` varchar(255) DEFAULT NULL COMMENT 'Nama Dusun',
  `village` varchar(255) DEFAULT NULL COMMENT 'Nama Kelurahan/ Desa',
  `sub_district` varchar(255) DEFAULT NULL COMMENT 'Kecamatan',
  `district` varchar(255) DEFAULT NULL COMMENT 'Kabupaten',
  `postal_code` varchar(20) DEFAULT NULL COMMENT 'Kode POS',
  `residence_id` bigint(20) DEFAULT 0 COMMENT 'Tempat Tinggal',
  `transportation_id` bigint(20) DEFAULT 0 COMMENT 'Moda Transportasi',
  `phone` varchar(50) DEFAULT NULL,
  `mobile_phone` varchar(50) DEFAULT NULL,
  `email` varchar(150) DEFAULT NULL,
  `sktm` varchar(100) DEFAULT NULL COMMENT 'Surat Keterangan Tidak Mampu (SKTM)',
  `kks` varchar(100) DEFAULT NULL COMMENT 'Kartu Keluarga Sejahtera (KKS)',
  `kps` varchar(100) DEFAULT NULL COMMENT 'Kartu Pra Sejahtera (KPS)',
  `kip` varchar(100) DEFAULT NULL COMMENT 'Kartu Indonesia Pintar (KIP)',
  `kis` varchar(100) DEFAULT NULL COMMENT 'Kartu Indonesia Sehat (KIS)',
  `citizenship` enum('WNI','WNA') NOT NULL DEFAULT 'WNI' COMMENT 'Kewarganegaraan',
  `country` varchar(255) DEFAULT NULL,
  `father_name` varchar(150) DEFAULT NULL,
  `father_birth_year` year(4) DEFAULT NULL,
  `father_education_id` bigint(20) DEFAULT 0,
  `father_employment_id` bigint(20) DEFAULT 0,
  `father_monthly_income_id` bigint(20) DEFAULT 0,
  `father_special_need_id` bigint(20) DEFAULT 0,
  `mother_name` varchar(150) DEFAULT NULL,
  `mother_birth_year` year(4) DEFAULT NULL,
  `mother_education_id` bigint(20) DEFAULT 0,
  `mother_employment_id` bigint(20) DEFAULT 0,
  `mother_monthly_income_id` bigint(20) DEFAULT 0,
  `mother_special_need_id` bigint(20) DEFAULT 0,
  `guardian_name` varchar(150) DEFAULT NULL,
  `guardian_birth_year` year(4) DEFAULT NULL,
  `guardian_education_id` bigint(20) DEFAULT 0,
  `guardian_employment_id` bigint(20) DEFAULT 0,
  `guardian_monthly_income_id` bigint(20) DEFAULT 0,
  `mileage` smallint(6) DEFAULT NULL COMMENT 'Jarak tempat tinggal ke sekolah',
  `traveling_time` smallint(6) DEFAULT NULL COMMENT 'Waktu Tempuh',
  `height` smallint(3) DEFAULT NULL COMMENT 'Tinggi Badan',
  `weight` smallint(3) DEFAULT NULL COMMENT 'Berat Badan',
  `sibling_number` smallint(2) DEFAULT 0 COMMENT 'Jumlah Saudara Kandng',
  `student_status_id` bigint(20) DEFAULT 0 COMMENT 'Status siswa',
  `end_date` date DEFAULT NULL COMMENT 'Tanggal Keluar',
  `reason` varchar(255) DEFAULT NULL COMMENT 'Diisi jika peserta didik sudah keluar',
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `subscribers`
--

CREATE TABLE `subscribers` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `email` varchar(255) DEFAULT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `tags`
--

CREATE TABLE `tags` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `tag` varchar(255) NOT NULL,
  `slug` varchar(255) DEFAULT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `tags`
--

INSERT INTO `tags` (`id`, `tag`, `slug`, `created_at`, `updated_at`, `deleted_at`, `restored_at`, `created_by`, `updated_by`, `deleted_by`, `restored_by`, `is_deleted`) VALUES
(1, 'Berita', 'berita', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(2, 'Pengumuman', 'pengumuman', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false'),
(3, 'Sekilas Info', 'sekilas-info', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 0, 0, 0, 0, 'false');

-- --------------------------------------------------------

--
-- Table structure for table `themes`
--

CREATE TABLE `themes` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `theme_name` varchar(255) NOT NULL,
  `theme_folder` varchar(255) DEFAULT NULL,
  `theme_author` varchar(255) DEFAULT NULL,
  `is_active` enum('true','false') DEFAULT 'false',
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `themes`
--

INSERT INTO `themes` (`id`, `theme_name`, `theme_folder`, `theme_author`, `is_active`, `created_at`, `updated_at`, `deleted_at`, `restored_at`, `created_by`, `updated_by`, `deleted_by`, `restored_by`, `is_deleted`) VALUES
(1, 'Sky Light', 'sky_light', 'Misdafatma Alza Astrafiyah', 'true', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 1, 0, 0, 0, 'false'),
(2, 'Blue Sky', 'blue_sky', 'Misdafatma Alza Astrafiyah', 'false', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 1, 0, 0, 0, 'false'),
(3, 'Green Land', 'green_land', 'Misdafatma Alza Astrafiyah', 'false', '2019-09-14 08:57:42', '2019-09-14 01:57:42', NULL, NULL, 1, 0, 0, 0, 'false');

-- --------------------------------------------------------

--
-- Table structure for table `users`
--

CREATE TABLE `users` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `user_name` varchar(60) NOT NULL,
  `user_password` varchar(100) NOT NULL,
  `user_full_name` varchar(100) DEFAULT NULL,
  `user_email` varchar(100) DEFAULT NULL,
  `user_url` varchar(100) DEFAULT NULL,
  `user_group_id` bigint(20) DEFAULT 0,
  `user_type` enum('super_user','administrator','employee','student') NOT NULL DEFAULT 'administrator',
  `user_profile_id` bigint(20) UNSIGNED DEFAULT NULL COMMENT 'student_id OR employee_id',
  `user_biography` text DEFAULT NULL,
  `user_forgot_password_key` varchar(100) DEFAULT NULL,
  `user_forgot_password_request_date` date DEFAULT NULL,
  `has_login` enum('true','false') DEFAULT 'false',
  `last_logged_in` datetime DEFAULT NULL,
  `ip_address` varchar(45) DEFAULT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `users`
--

INSERT INTO `users` (`id`, `user_name`, `user_password`, `user_full_name`, `user_email`, `user_url`, `user_group_id`, `user_type`, `user_profile_id`, `user_biography`, `user_forgot_password_key`, `user_forgot_password_request_date`, `has_login`, `last_logged_in`, `ip_address`, `created_at`, `updated_at`, `deleted_at`, `restored_at`, `created_by`, `updated_by`, `deleted_by`, `restored_by`, `is_deleted`) VALUES
(1, 'administrator', '$2y$10$Sn.VbUb5IdtUN3oAvNb3TettKbi5dpfGI9sL1ZFLmSzZAOd3M7UxG', 'Administrator', 'misdafatmaa@gmail.com', 'linktr.ee/misda_masda', 0, 'super_user', NULL, NULL, NULL, NULL, 'false', NULL, NULL, '2019-09-14 08:57:42', '2021-08-05 08:47:14', NULL, NULL, 0, 0, 0, 0, 'false');

-- --------------------------------------------------------

--
-- Table structure for table `user_groups`
--

CREATE TABLE `user_groups` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `user_group` varchar(255) NOT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `user_privileges`
--

CREATE TABLE `user_privileges` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `user_group_id` bigint(20) DEFAULT 0,
  `module_id` bigint(20) DEFAULT 0,
  `created_at` datetime DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `deleted_at` datetime DEFAULT NULL,
  `restored_at` datetime DEFAULT NULL,
  `created_by` bigint(20) DEFAULT 0,
  `updated_by` bigint(20) DEFAULT 0,
  `deleted_by` bigint(20) DEFAULT 0,
  `restored_by` bigint(20) DEFAULT 0,
  `is_deleted` enum('true','false') DEFAULT 'false'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- --------------------------------------------------------

--
-- Table structure for table `_sessions`
--

CREATE TABLE `_sessions` (
  `id` varchar(128) NOT NULL,
  `ip_address` varchar(45) NOT NULL,
  `timestamp` int(10) UNSIGNED NOT NULL DEFAULT 0,
  `data` blob NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Indexes for dumped tables
--

--
-- Indexes for table `academic_years`
--
ALTER TABLE `academic_years`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `academic_year` (`academic_year`);

--
-- Indexes for table `achievements`
--
ALTER TABLE `achievements`
  ADD PRIMARY KEY (`id`),
  ADD KEY `achievements_student_id__idx` (`student_id`) USING BTREE;

--
-- Indexes for table `admission_phases`
--
ALTER TABLE `admission_phases`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `unique_field` (`academic_year_id`,`phase_name`),
  ADD KEY `admission_phases_academic_year_id__idx` (`academic_year_id`) USING BTREE;

--
-- Indexes for table `admission_quotas`
--
ALTER TABLE `admission_quotas`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `unique_field` (`academic_year_id`,`admission_type_id`,`major_id`),
  ADD KEY `admission_quotas_academic_year_id__idx` (`academic_year_id`) USING BTREE,
  ADD KEY `admission_quotas_admission_type_id__idx` (`admission_type_id`) USING BTREE,
  ADD KEY `admission_quotas_major_id__idx` (`major_id`) USING BTREE;

--
-- Indexes for table `albums`
--
ALTER TABLE `albums`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `album_title` (`album_title`);

--
-- Indexes for table `answers`
--
ALTER TABLE `answers`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `unique_field` (`question_id`,`answer`),
  ADD KEY `answers_question_id__idx` (`question_id`) USING BTREE;

--
-- Indexes for table `categories`
--
ALTER TABLE `categories`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `unique_field` (`category_name`,`category_type`);

--
-- Indexes for table `class_groups`
--
ALTER TABLE `class_groups`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `unique_field` (`class_group`,`sub_class_group`,`major_id`),
  ADD KEY `class_groups_major_id__idx` (`major_id`) USING BTREE;

--
-- Indexes for table `class_group_settings`
--
ALTER TABLE `class_group_settings`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `unique_field` (`academic_year_id`,`class_group_id`),
  ADD KEY `class_group_settings_academic_year_id__idx` (`academic_year_id`) USING BTREE,
  ADD KEY `class_group_settings_class_group_id__idx` (`class_group_id`) USING BTREE;

--
-- Indexes for table `class_group_students`
--
ALTER TABLE `class_group_students`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `unique_field` (`class_group_setting_id`,`student_id`),
  ADD KEY `class_group_students_class_group_setting_id__idx` (`class_group_setting_id`) USING BTREE,
  ADD KEY `class_group_students_student_id__idx` (`student_id`) USING BTREE;

--
-- Indexes for table `comments`
--
ALTER TABLE `comments`
  ADD PRIMARY KEY (`id`),
  ADD KEY `comments_comment_post_id__idx` (`comment_post_id`) USING BTREE;

--
-- Indexes for table `employees`
--
ALTER TABLE `employees`
  ADD PRIMARY KEY (`id`),
  ADD KEY `employees_nik__idx` (`nik`) USING BTREE,
  ADD KEY `employees_full_name__idx` (`full_name`) USING BTREE,
  ADD KEY `employees_email__idx` (`email`) USING BTREE,
  ADD KEY `employees_religion_id__idx` (`religion_id`) USING BTREE,
  ADD KEY `employees_marriage_status_id__idx` (`marriage_status_id`) USING BTREE,
  ADD KEY `employees_spouse_employment_id__idx` (`spouse_employment_id`) USING BTREE,
  ADD KEY `employees_employment_status_id__idx` (`employment_status_id`) USING BTREE,
  ADD KEY `employees_employment_type_id__idx` (`employment_type_id`) USING BTREE,
  ADD KEY `employees_institution_lifter_id__idx` (`institution_lifter_id`) USING BTREE,
  ADD KEY `employees_rank_id__idx` (`rank_id`) USING BTREE,
  ADD KEY `employees_salary_source_id__idx` (`salary_source_id`) USING BTREE,
  ADD KEY `employees_laboratory_skill_id__idx` (`laboratory_skill_id`) USING BTREE,
  ADD KEY `employees_special_need_id__idx` (`special_need_id`) USING BTREE;

--
-- Indexes for table `files`
--
ALTER TABLE `files`
  ADD PRIMARY KEY (`id`),
  ADD KEY `files_file_category_id__idx` (`file_category_id`) USING BTREE;

--
-- Indexes for table `image_sliders`
--
ALTER TABLE `image_sliders`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `links`
--
ALTER TABLE `links`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `unique_field` (`link_url`,`link_type`);

--
-- Indexes for table `login_attempts`
--
ALTER TABLE `login_attempts`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `majors`
--
ALTER TABLE `majors`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `major_name` (`major_name`);

--
-- Indexes for table `menus`
--
ALTER TABLE `menus`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `modules`
--
ALTER TABLE `modules`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `module_name` (`module_name`);

--
-- Indexes for table `options`
--
ALTER TABLE `options`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `unique_field` (`option_group`,`option_name`),
  ADD KEY `options_option_group__idx` (`option_group`) USING BTREE;

--
-- Indexes for table `photos`
--
ALTER TABLE `photos`
  ADD PRIMARY KEY (`id`),
  ADD KEY `photos_photo_album_id__idx` (`photo_album_id`) USING BTREE;

--
-- Indexes for table `pollings`
--
ALTER TABLE `pollings`
  ADD PRIMARY KEY (`id`),
  ADD KEY `pollings_answer_id__idx` (`answer_id`) USING BTREE;

--
-- Indexes for table `posts`
--
ALTER TABLE `posts`
  ADD PRIMARY KEY (`id`),
  ADD KEY `posts_post_author__idx` (`post_author`) USING BTREE;

--
-- Indexes for table `questions`
--
ALTER TABLE `questions`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `question` (`question`);

--
-- Indexes for table `quotes`
--
ALTER TABLE `quotes`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `unique_field` (`quote`,`quote_by`);

--
-- Indexes for table `scholarships`
--
ALTER TABLE `scholarships`
  ADD PRIMARY KEY (`id`),
  ADD KEY `scholarships_student_id__idx` (`student_id`) USING BTREE;

--
-- Indexes for table `settings`
--
ALTER TABLE `settings`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `unique_field` (`setting_group`,`setting_variable`);

--
-- Indexes for table `students`
--
ALTER TABLE `students`
  ADD PRIMARY KEY (`id`),
  ADD KEY `students_registration_number__idx` (`registration_number`) USING BTREE,
  ADD KEY `students_identity_number__idx` (`identity_number`) USING BTREE,
  ADD KEY `students_full_name__idx` (`full_name`) USING BTREE,
  ADD KEY `students_first_choice_id__idx` (`first_choice_id`) USING BTREE,
  ADD KEY `students_second_choice_id__idx` (`second_choice_id`) USING BTREE,
  ADD KEY `students_major_id__idx` (`major_id`) USING BTREE,
  ADD KEY `students_admission_phase_id__idx` (`admission_phase_id`) USING BTREE,
  ADD KEY `students_admission_type_id__idx` (`admission_type_id`) USING BTREE,
  ADD KEY `students_student_status_id__idx` (`student_status_id`) USING BTREE;

--
-- Indexes for table `subscribers`
--
ALTER TABLE `subscribers`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `email` (`email`);

--
-- Indexes for table `tags`
--
ALTER TABLE `tags`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `tag` (`tag`);

--
-- Indexes for table `themes`
--
ALTER TABLE `themes`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `theme_name` (`theme_name`);

--
-- Indexes for table `users`
--
ALTER TABLE `users`
  ADD PRIMARY KEY (`id`),
  ADD KEY `users_user_group_id__idx` (`user_group_id`) USING BTREE,
  ADD KEY `users_user_profile_id__idx` (`user_profile_id`) USING BTREE;

--
-- Indexes for table `user_groups`
--
ALTER TABLE `user_groups`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `user_group` (`user_group`);

--
-- Indexes for table `user_privileges`
--
ALTER TABLE `user_privileges`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `unique_field` (`user_group_id`,`module_id`),
  ADD KEY `user_privileges_user_group_id__idx` (`user_group_id`) USING BTREE,
  ADD KEY `user_privileges_module_id__idx` (`module_id`) USING BTREE;

--
-- Indexes for table `_sessions`
--
ALTER TABLE `_sessions`
  ADD KEY `ci_sessions_TIMESTAMP` (`timestamp`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `academic_years`
--
ALTER TABLE `academic_years`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `achievements`
--
ALTER TABLE `achievements`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `admission_phases`
--
ALTER TABLE `admission_phases`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `admission_quotas`
--
ALTER TABLE `admission_quotas`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `albums`
--
ALTER TABLE `albums`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `answers`
--
ALTER TABLE `answers`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `categories`
--
ALTER TABLE `categories`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=3;

--
-- AUTO_INCREMENT for table `class_groups`
--
ALTER TABLE `class_groups`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `class_group_settings`
--
ALTER TABLE `class_group_settings`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `class_group_students`
--
ALTER TABLE `class_group_students`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `comments`
--
ALTER TABLE `comments`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `employees`
--
ALTER TABLE `employees`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `files`
--
ALTER TABLE `files`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `image_sliders`
--
ALTER TABLE `image_sliders`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=3;

--
-- AUTO_INCREMENT for table `links`
--
ALTER TABLE `links`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=3;

--
-- AUTO_INCREMENT for table `login_attempts`
--
ALTER TABLE `login_attempts`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `majors`
--
ALTER TABLE `majors`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `menus`
--
ALTER TABLE `menus`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=19;

--
-- AUTO_INCREMENT for table `modules`
--
ALTER TABLE `modules`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=11;

--
-- AUTO_INCREMENT for table `options`
--
ALTER TABLE `options`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=170;

--
-- AUTO_INCREMENT for table `photos`
--
ALTER TABLE `photos`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `pollings`
--
ALTER TABLE `pollings`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `posts`
--
ALTER TABLE `posts`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=9;

--
-- AUTO_INCREMENT for table `questions`
--
ALTER TABLE `questions`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `quotes`
--
ALTER TABLE `quotes`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=4;

--
-- AUTO_INCREMENT for table `scholarships`
--
ALTER TABLE `scholarships`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `settings`
--
ALTER TABLE `settings`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=93;

--
-- AUTO_INCREMENT for table `students`
--
ALTER TABLE `students`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `subscribers`
--
ALTER TABLE `subscribers`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `tags`
--
ALTER TABLE `tags`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=4;

--
-- AUTO_INCREMENT for table `themes`
--
ALTER TABLE `themes`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=4;

--
-- AUTO_INCREMENT for table `users`
--
ALTER TABLE `users`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;

--
-- AUTO_INCREMENT for table `user_groups`
--
ALTER TABLE `user_groups`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `user_privileges`
--
ALTER TABLE `user_privileges`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;
--
-- Database: `astracomputer`
--
CREATE DATABASE IF NOT EXISTS `astracomputer` DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci;
USE `astracomputer`;
--
-- Database: `phpmyadmin`
--
CREATE DATABASE IF NOT EXISTS `phpmyadmin` DEFAULT CHARACTER SET utf8 COLLATE utf8_bin;
USE `phpmyadmin`;

-- --------------------------------------------------------

--
-- Table structure for table `pma__bookmark`
--

CREATE TABLE `pma__bookmark` (
  `id` int(10) UNSIGNED NOT NULL,
  `dbase` varchar(255) COLLATE utf8_bin NOT NULL DEFAULT '',
  `user` varchar(255) COLLATE utf8_bin NOT NULL DEFAULT '',
  `label` varchar(255) CHARACTER SET utf8 NOT NULL DEFAULT '',
  `query` text COLLATE utf8_bin NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='Bookmarks';

-- --------------------------------------------------------

--
-- Table structure for table `pma__central_columns`
--

CREATE TABLE `pma__central_columns` (
  `db_name` varchar(64) COLLATE utf8_bin NOT NULL,
  `col_name` varchar(64) COLLATE utf8_bin NOT NULL,
  `col_type` varchar(64) COLLATE utf8_bin NOT NULL,
  `col_length` text COLLATE utf8_bin DEFAULT NULL,
  `col_collation` varchar(64) COLLATE utf8_bin NOT NULL,
  `col_isNull` tinyint(1) NOT NULL,
  `col_extra` varchar(255) COLLATE utf8_bin DEFAULT '',
  `col_default` text COLLATE utf8_bin DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='Central list of columns';

-- --------------------------------------------------------

--
-- Table structure for table `pma__column_info`
--

CREATE TABLE `pma__column_info` (
  `id` int(5) UNSIGNED NOT NULL,
  `db_name` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `table_name` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `column_name` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `comment` varchar(255) CHARACTER SET utf8 NOT NULL DEFAULT '',
  `mimetype` varchar(255) CHARACTER SET utf8 NOT NULL DEFAULT '',
  `transformation` varchar(255) COLLATE utf8_bin NOT NULL DEFAULT '',
  `transformation_options` varchar(255) COLLATE utf8_bin NOT NULL DEFAULT '',
  `input_transformation` varchar(255) COLLATE utf8_bin NOT NULL DEFAULT '',
  `input_transformation_options` varchar(255) COLLATE utf8_bin NOT NULL DEFAULT ''
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='Column information for phpMyAdmin';

-- --------------------------------------------------------

--
-- Table structure for table `pma__designer_settings`
--

CREATE TABLE `pma__designer_settings` (
  `username` varchar(64) COLLATE utf8_bin NOT NULL,
  `settings_data` text COLLATE utf8_bin NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='Settings related to Designer';

-- --------------------------------------------------------

--
-- Table structure for table `pma__export_templates`
--

CREATE TABLE `pma__export_templates` (
  `id` int(5) UNSIGNED NOT NULL,
  `username` varchar(64) COLLATE utf8_bin NOT NULL,
  `export_type` varchar(10) COLLATE utf8_bin NOT NULL,
  `template_name` varchar(64) COLLATE utf8_bin NOT NULL,
  `template_data` text COLLATE utf8_bin NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='Saved export templates';

--
-- Dumping data for table `pma__export_templates`
--

INSERT INTO `pma__export_templates` (`id`, `username`, `export_type`, `template_name`, `template_data`) VALUES
(1, 'root', 'server', 'Astra Computer', '{\"quick_or_custom\":\"quick\",\"what\":\"sql\",\"db_select[]\":[\"astra computer\",\"astracomputer\",\"phpmyadmin\",\"test\"],\"aliases_new\":\"\",\"output_format\":\"sendit\",\"filename_template\":\"@SERVER@\",\"remember_template\":\"on\",\"charset\":\"utf-8\",\"compression\":\"none\",\"maxsize\":\"\",\"codegen_structure_or_data\":\"data\",\"codegen_format\":\"0\",\"csv_separator\":\",\",\"csv_enclosed\":\"\\\"\",\"csv_escaped\":\"\\\"\",\"csv_terminated\":\"AUTO\",\"csv_null\":\"NULL\",\"csv_structure_or_data\":\"data\",\"excel_null\":\"NULL\",\"excel_columns\":\"something\",\"excel_edition\":\"win\",\"excel_structure_or_data\":\"data\",\"json_structure_or_data\":\"data\",\"json_unicode\":\"something\",\"latex_caption\":\"something\",\"latex_structure_or_data\":\"structure_and_data\",\"latex_structure_caption\":\"Structure of table @TABLE@\",\"latex_structure_continued_caption\":\"Structure of table @TABLE@ (continued)\",\"latex_structure_label\":\"tab:@TABLE@-structure\",\"latex_relation\":\"something\",\"latex_comments\":\"something\",\"latex_mime\":\"something\",\"latex_columns\":\"something\",\"latex_data_caption\":\"Content of table @TABLE@\",\"latex_data_continued_caption\":\"Content of table @TABLE@ (continued)\",\"latex_data_label\":\"tab:@TABLE@-data\",\"latex_null\":\"\\\\textit{NULL}\",\"mediawiki_structure_or_data\":\"data\",\"mediawiki_caption\":\"something\",\"mediawiki_headers\":\"something\",\"htmlword_structure_or_data\":\"structure_and_data\",\"htmlword_null\":\"NULL\",\"ods_null\":\"NULL\",\"ods_structure_or_data\":\"data\",\"odt_structure_or_data\":\"structure_and_data\",\"odt_relation\":\"something\",\"odt_comments\":\"something\",\"odt_mime\":\"something\",\"odt_columns\":\"something\",\"odt_null\":\"NULL\",\"pdf_report_title\":\"\",\"pdf_structure_or_data\":\"data\",\"phparray_structure_or_data\":\"data\",\"sql_include_comments\":\"something\",\"sql_header_comment\":\"\",\"sql_use_transaction\":\"something\",\"sql_compatibility\":\"NONE\",\"sql_structure_or_data\":\"structure_and_data\",\"sql_create_table\":\"something\",\"sql_auto_increment\":\"something\",\"sql_create_view\":\"something\",\"sql_create_trigger\":\"something\",\"sql_backquotes\":\"something\",\"sql_type\":\"INSERT\",\"sql_insert_syntax\":\"both\",\"sql_max_query_size\":\"50000\",\"sql_hex_for_binary\":\"something\",\"sql_utc_time\":\"something\",\"texytext_structure_or_data\":\"structure_and_data\",\"texytext_null\":\"NULL\",\"yaml_structure_or_data\":\"data\",\"\":null,\"as_separate_files\":null,\"csv_removeCRLF\":null,\"csv_columns\":null,\"excel_removeCRLF\":null,\"json_pretty_print\":null,\"htmlword_columns\":null,\"ods_columns\":null,\"sql_dates\":null,\"sql_relation\":null,\"sql_mime\":null,\"sql_disable_fk\":null,\"sql_views_as_tables\":null,\"sql_metadata\":null,\"sql_drop_database\":null,\"sql_drop_table\":null,\"sql_if_not_exists\":null,\"sql_simple_view_export\":null,\"sql_view_current_user\":null,\"sql_or_replace_view\":null,\"sql_procedure_function\":null,\"sql_truncate\":null,\"sql_delayed\":null,\"sql_ignore\":null,\"texytext_columns\":null}');

-- --------------------------------------------------------

--
-- Table structure for table `pma__favorite`
--

CREATE TABLE `pma__favorite` (
  `username` varchar(64) COLLATE utf8_bin NOT NULL,
  `tables` text COLLATE utf8_bin NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='Favorite tables';

-- --------------------------------------------------------

--
-- Table structure for table `pma__history`
--

CREATE TABLE `pma__history` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `username` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `db` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `table` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `timevalue` timestamp NOT NULL DEFAULT current_timestamp(),
  `sqlquery` text COLLATE utf8_bin NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='SQL history for phpMyAdmin';

-- --------------------------------------------------------

--
-- Table structure for table `pma__navigationhiding`
--

CREATE TABLE `pma__navigationhiding` (
  `username` varchar(64) COLLATE utf8_bin NOT NULL,
  `item_name` varchar(64) COLLATE utf8_bin NOT NULL,
  `item_type` varchar(64) COLLATE utf8_bin NOT NULL,
  `db_name` varchar(64) COLLATE utf8_bin NOT NULL,
  `table_name` varchar(64) COLLATE utf8_bin NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='Hidden items of navigation tree';

-- --------------------------------------------------------

--
-- Table structure for table `pma__pdf_pages`
--

CREATE TABLE `pma__pdf_pages` (
  `db_name` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `page_nr` int(10) UNSIGNED NOT NULL,
  `page_descr` varchar(50) CHARACTER SET utf8 NOT NULL DEFAULT ''
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='PDF relation pages for phpMyAdmin';

-- --------------------------------------------------------

--
-- Table structure for table `pma__recent`
--

CREATE TABLE `pma__recent` (
  `username` varchar(64) COLLATE utf8_bin NOT NULL,
  `tables` text COLLATE utf8_bin NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='Recently accessed tables';

--
-- Dumping data for table `pma__recent`
--

INSERT INTO `pma__recent` (`username`, `tables`) VALUES
('root', '[{\"db\":\"astra computer\",\"table\":\"users\"}]');

-- --------------------------------------------------------

--
-- Table structure for table `pma__relation`
--

CREATE TABLE `pma__relation` (
  `master_db` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `master_table` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `master_field` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `foreign_db` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `foreign_table` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `foreign_field` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT ''
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='Relation table';

-- --------------------------------------------------------

--
-- Table structure for table `pma__savedsearches`
--

CREATE TABLE `pma__savedsearches` (
  `id` int(5) UNSIGNED NOT NULL,
  `username` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `db_name` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `search_name` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `search_data` text COLLATE utf8_bin NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='Saved searches';

-- --------------------------------------------------------

--
-- Table structure for table `pma__table_coords`
--

CREATE TABLE `pma__table_coords` (
  `db_name` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `table_name` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `pdf_page_number` int(11) NOT NULL DEFAULT 0,
  `x` float UNSIGNED NOT NULL DEFAULT 0,
  `y` float UNSIGNED NOT NULL DEFAULT 0
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='Table coordinates for phpMyAdmin PDF output';

-- --------------------------------------------------------

--
-- Table structure for table `pma__table_info`
--

CREATE TABLE `pma__table_info` (
  `db_name` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `table_name` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT '',
  `display_field` varchar(64) COLLATE utf8_bin NOT NULL DEFAULT ''
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='Table information for phpMyAdmin';

-- --------------------------------------------------------

--
-- Table structure for table `pma__table_uiprefs`
--

CREATE TABLE `pma__table_uiprefs` (
  `username` varchar(64) COLLATE utf8_bin NOT NULL,
  `db_name` varchar(64) COLLATE utf8_bin NOT NULL,
  `table_name` varchar(64) COLLATE utf8_bin NOT NULL,
  `prefs` text COLLATE utf8_bin NOT NULL,
  `last_update` timestamp NOT NULL DEFAULT current_timestamp() ON UPDATE current_timestamp()
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='Tables'' UI preferences';

-- --------------------------------------------------------

--
-- Table structure for table `pma__tracking`
--

CREATE TABLE `pma__tracking` (
  `db_name` varchar(64) COLLATE utf8_bin NOT NULL,
  `table_name` varchar(64) COLLATE utf8_bin NOT NULL,
  `version` int(10) UNSIGNED NOT NULL,
  `date_created` datetime NOT NULL,
  `date_updated` datetime NOT NULL,
  `schema_snapshot` text COLLATE utf8_bin NOT NULL,
  `schema_sql` text COLLATE utf8_bin DEFAULT NULL,
  `data_sql` longtext COLLATE utf8_bin DEFAULT NULL,
  `tracking` set('UPDATE','REPLACE','INSERT','DELETE','TRUNCATE','CREATE DATABASE','ALTER DATABASE','DROP DATABASE','CREATE TABLE','ALTER TABLE','RENAME TABLE','DROP TABLE','CREATE INDEX','DROP INDEX','CREATE VIEW','ALTER VIEW','DROP VIEW') COLLATE utf8_bin DEFAULT NULL,
  `tracking_active` int(1) UNSIGNED NOT NULL DEFAULT 1
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='Database changes tracking for phpMyAdmin';

-- --------------------------------------------------------

--
-- Table structure for table `pma__userconfig`
--

CREATE TABLE `pma__userconfig` (
  `username` varchar(64) COLLATE utf8_bin NOT NULL,
  `timevalue` timestamp NOT NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `config_data` text COLLATE utf8_bin NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='User preferences storage for phpMyAdmin';

--
-- Dumping data for table `pma__userconfig`
--

INSERT INTO `pma__userconfig` (`username`, `timevalue`, `config_data`) VALUES
('root', '2021-08-05 08:45:39', '{\"Console\\/Mode\":\"collapse\"}');

-- --------------------------------------------------------

--
-- Table structure for table `pma__usergroups`
--

CREATE TABLE `pma__usergroups` (
  `usergroup` varchar(64) COLLATE utf8_bin NOT NULL,
  `tab` varchar(64) COLLATE utf8_bin NOT NULL,
  `allowed` enum('Y','N') COLLATE utf8_bin NOT NULL DEFAULT 'N'
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='User groups with configured menu items';

-- --------------------------------------------------------

--
-- Table structure for table `pma__users`
--

CREATE TABLE `pma__users` (
  `username` varchar(64) COLLATE utf8_bin NOT NULL,
  `usergroup` varchar(64) COLLATE utf8_bin NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin COMMENT='Users and their assignments to user groups';

--
-- Indexes for dumped tables
--

--
-- Indexes for table `pma__bookmark`
--
ALTER TABLE `pma__bookmark`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `pma__central_columns`
--
ALTER TABLE `pma__central_columns`
  ADD PRIMARY KEY (`db_name`,`col_name`);

--
-- Indexes for table `pma__column_info`
--
ALTER TABLE `pma__column_info`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `db_name` (`db_name`,`table_name`,`column_name`);

--
-- Indexes for table `pma__designer_settings`
--
ALTER TABLE `pma__designer_settings`
  ADD PRIMARY KEY (`username`);

--
-- Indexes for table `pma__export_templates`
--
ALTER TABLE `pma__export_templates`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `u_user_type_template` (`username`,`export_type`,`template_name`);

--
-- Indexes for table `pma__favorite`
--
ALTER TABLE `pma__favorite`
  ADD PRIMARY KEY (`username`);

--
-- Indexes for table `pma__history`
--
ALTER TABLE `pma__history`
  ADD PRIMARY KEY (`id`),
  ADD KEY `username` (`username`,`db`,`table`,`timevalue`);

--
-- Indexes for table `pma__navigationhiding`
--
ALTER TABLE `pma__navigationhiding`
  ADD PRIMARY KEY (`username`,`item_name`,`item_type`,`db_name`,`table_name`);

--
-- Indexes for table `pma__pdf_pages`
--
ALTER TABLE `pma__pdf_pages`
  ADD PRIMARY KEY (`page_nr`),
  ADD KEY `db_name` (`db_name`);

--
-- Indexes for table `pma__recent`
--
ALTER TABLE `pma__recent`
  ADD PRIMARY KEY (`username`);

--
-- Indexes for table `pma__relation`
--
ALTER TABLE `pma__relation`
  ADD PRIMARY KEY (`master_db`,`master_table`,`master_field`),
  ADD KEY `foreign_field` (`foreign_db`,`foreign_table`);

--
-- Indexes for table `pma__savedsearches`
--
ALTER TABLE `pma__savedsearches`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `u_savedsearches_username_dbname` (`username`,`db_name`,`search_name`);

--
-- Indexes for table `pma__table_coords`
--
ALTER TABLE `pma__table_coords`
  ADD PRIMARY KEY (`db_name`,`table_name`,`pdf_page_number`);

--
-- Indexes for table `pma__table_info`
--
ALTER TABLE `pma__table_info`
  ADD PRIMARY KEY (`db_name`,`table_name`);

--
-- Indexes for table `pma__table_uiprefs`
--
ALTER TABLE `pma__table_uiprefs`
  ADD PRIMARY KEY (`username`,`db_name`,`table_name`);

--
-- Indexes for table `pma__tracking`
--
ALTER TABLE `pma__tracking`
  ADD PRIMARY KEY (`db_name`,`table_name`,`version`);

--
-- Indexes for table `pma__userconfig`
--
ALTER TABLE `pma__userconfig`
  ADD PRIMARY KEY (`username`);

--
-- Indexes for table `pma__usergroups`
--
ALTER TABLE `pma__usergroups`
  ADD PRIMARY KEY (`usergroup`,`tab`,`allowed`);

--
-- Indexes for table `pma__users`
--
ALTER TABLE `pma__users`
  ADD PRIMARY KEY (`username`,`usergroup`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `pma__bookmark`
--
ALTER TABLE `pma__bookmark`
  MODIFY `id` int(10) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `pma__column_info`
--
ALTER TABLE `pma__column_info`
  MODIFY `id` int(5) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `pma__export_templates`
--
ALTER TABLE `pma__export_templates`
  MODIFY `id` int(5) UNSIGNED NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;

--
-- AUTO_INCREMENT for table `pma__history`
--
ALTER TABLE `pma__history`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `pma__pdf_pages`
--
ALTER TABLE `pma__pdf_pages`
  MODIFY `page_nr` int(10) UNSIGNED NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `pma__savedsearches`
--
ALTER TABLE `pma__savedsearches`
  MODIFY `id` int(5) UNSIGNED NOT NULL AUTO_INCREMENT;
--
-- Database: `test`
--
CREATE DATABASE IF NOT EXISTS `test` DEFAULT CHARACTER SET latin1 COLLATE latin1_swedish_ci;
USE `test`;
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
