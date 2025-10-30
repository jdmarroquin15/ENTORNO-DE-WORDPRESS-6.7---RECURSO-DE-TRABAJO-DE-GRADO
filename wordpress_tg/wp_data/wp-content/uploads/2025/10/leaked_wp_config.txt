<?php
define( 'WP_CACHE', true );
/**
 * The base configuration for WordPress
 *
 * The wp-config.php creation script uses this file during the installation.
 * You don't have to use the website, you can copy this file to "wp-config.php"
 * and fill in the values.
 *
 * This file contains the following configurations:
 *
 * * Database settings
 * * Secret keys
 * * Database table prefix
 * * ABSPATH
 *
 * @link https://developer.wordpress.org/advanced-administration/wordpress/wp-config/
 *
 * @package WordPress
 */

// ** Database settings - You can get this info from your web host ** //
/** The name of the database for WordPress */
define( 'DB_NAME', 'wpdb' );

/** Database username */
define( 'DB_USER', 'wpuser' );

/** Database password */
define( 'DB_PASSWORD', 'wppassword' );

/** Database hostname */
define( 'DB_HOST', 'wordpress_db' );

/** Database charset to use in creating database tables. */
define( 'DB_CHARSET', 'utf8mb4' );

/** The database collate type. Don't change this if in doubt. */
define( 'DB_COLLATE', '' );

/**#@+
 * Authentication unique keys and salts.
 *
 * Change these to different unique phrases! You can generate these using
 * the {@link https://api.wordpress.org/secret-key/1.1/salt/ WordPress.org secret-key service}.
 *
 * You can change these at any point in time to invalidate all existing cookies.
 * This will force all users to have to log in again.
 *
 * @since 2.6.0
 */
define( 'AUTH_KEY',         'N:X8k6zt2qzk)mcL@}fhEg2#l)C>lpt2E/4>e?a.O=xi#1:Z^qXd:-_i}grzAPqP' );
define( 'SECURE_AUTH_KEY',  'y>!lRpr}v0q-~?p^DawY$d^,v|S;zvwg%:@/c|dCX+p/RDU/_7j0iX/Xk9r(ZSm@' );
define( 'LOGGED_IN_KEY',    '?~4hS[UDLOb!%8v-cfDWjfUl^8DK#[<{#G#zLy<^-a&)oK$;9$L@]-fzoW`^(96A' );
define( 'NONCE_KEY',        'yX[=5mX!.Am^*I6&7AyW827Qn}|u*Qq.dSFKa(mge`Q ]D:$[tyj&4O[6xup? N|' );
define( 'AUTH_SALT',        'y$mwII1=nMiPw$ L^ZCp9j21oLElHkw|^}+Kp,X,fl?3V!YvEN66^/Cc!y8:a{cs' );
define( 'SECURE_AUTH_SALT', 'hS=qbfm2^)Onal62q8<~n31,uIloI1Iw]4/!+CO,F?tjC=hY+7w1mB~bN>5SXz8;' );
define( 'LOGGED_IN_SALT',   'mXf`W*YP]G4c>xdrc/Dy5Au`J5J3KB;!Zw^-lr@zS[pY$?Pn;HJ<qj]l;$~@vR&g' );
define( 'NONCE_SALT',       '.l9|_3Qex&+4!?e~HITinR}{5k0jL<7ej g9MhAjgXJZMm}3y5-I%*#w/f3;B Z0' );

/**#@-*/

/**
 * WordPress database table prefix.
 *
 * You can have multiple installations in one database if you give each
 * a unique prefix. Only numbers, letters, and underscores please!
 *
 * At the installation time, database tables are created with the specified prefix.
 * Changing this value after WordPress is installed will make your site think
 * it has not been installed.
 *
 * @link https://developer.wordpress.org/advanced-administration/wordpress/wp-config/#table-prefix
 */
$table_prefix = 'wp_';

/**
 * For developers: WordPress debugging mode.
 *
 * Change this to true to enable the display of notices during development.
 * It is strongly recommended that plugin and theme developers use WP_DEBUG
 * in their development environments.
 *
 * For information on other constants that can be used for debugging,
 * visit the documentation.
 *
 * @link https://developer.wordpress.org/advanced-administration/debug/debug-wordpress/
 */
define( 'WP_DEBUG', false );

/* Add any custom values between this line and the "stop editing" line. */



/* That's all, stop editing! Happy publishing. */

/** Absolute path to the WordPress directory. */
if ( ! defined( 'ABSPATH' ) ) {
	define( 'ABSPATH', __DIR__ . '/' );
}

/** Sets up WordPress vars and included files. */
require_once ABSPATH . 'wp-settings.php';
