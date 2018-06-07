---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: a00bc2f13117f1b07f0dcc5808eddbabe1df940f
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821667"
---
# <a name="release-notes"></a><span data-ttu-id="23731-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="23731-103">Release notes</span></span>

<span data-ttu-id="23731-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="23731-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-220"></a><span data-ttu-id="23731-105">Versione 2.2.0</span><span class="sxs-lookup"><span data-stu-id="23731-105">Version 2.2.0</span></span>
* <span data-ttu-id="23731-106">Calcolo</span><span class="sxs-lookup"><span data-stu-id="23731-106">Compute</span></span>
  - <span data-ttu-id="23731-107">Aggiunta del supporto per l'esecuzione di query sullo stato di crittografia dall'estensione AzureDiskEncryptionForLinux</span><span class="sxs-lookup"><span data-stu-id="23731-107">Add support for querying encryption status from the AzureDiskEncryptionForLinux extension</span></span>
* <span data-ttu-id="23731-108">DataFactory</span><span class="sxs-lookup"><span data-stu-id="23731-108">DataFactory</span></span>
  - <span data-ttu-id="23731-109">Aggiunta di un nuovo cmdlet per elencare le finestre attività</span><span class="sxs-lookup"><span data-stu-id="23731-109">Added new cmdlet for listing activity windows</span></span>
    + <span data-ttu-id="23731-110">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="23731-110">Get-AzureRmDataFactoryActivityWindow</span></span>
* <span data-ttu-id="23731-111">DataLake</span><span class="sxs-lookup"><span data-stu-id="23731-111">DataLake</span></span>
  - <span data-ttu-id="23731-112">Modifica del parametro `Host` in `DatabaseHost` e aggiunta dell'alias a `Host`</span><span class="sxs-lookup"><span data-stu-id="23731-112">Changed parameter `Host` to `DatabaseHost` and added alias to `Host`</span></span>
    + <span data-ttu-id="23731-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="23731-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
    + <span data-ttu-id="23731-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="23731-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
  - <span data-ttu-id="23731-115">Aggiunta del supporto per la rimozione di ACL e ACL predefiniti</span><span class="sxs-lookup"><span data-stu-id="23731-115">Add support for ACL and Default ACL removal</span></span>
  - <span data-ttu-id="23731-116">Aggiunta del supporto per ottenere e impostare autorizzazioni senza nome per file e cartelle</span><span class="sxs-lookup"><span data-stu-id="23731-116">Add support for getting and setting unnamed permissions on files and folders</span></span>
* <span data-ttu-id="23731-117">Insieme di credenziali delle chiavi</span><span class="sxs-lookup"><span data-stu-id="23731-117">KeyVault</span></span>
  - <span data-ttu-id="23731-118">Aggiunta del supporto per certificati</span><span class="sxs-lookup"><span data-stu-id="23731-118">Add support for certificates</span></span>
    + <span data-ttu-id="23731-119">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="23731-119">Add-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="23731-120">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="23731-120">Add-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="23731-121">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="23731-121">Get-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="23731-122">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="23731-122">Get-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="23731-123">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="23731-123">Get-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="23731-124">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="23731-124">Get-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="23731-125">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="23731-125">Get-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="23731-126">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="23731-126">Import-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="23731-127">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="23731-127">New-AzureKeyVaultCertificateAdministratorDetails</span></span>
    + <span data-ttu-id="23731-128">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="23731-128">New-AzureKeyVaultCertificateOrganizationDetails</span></span>
    + <span data-ttu-id="23731-129">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="23731-129">New-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="23731-130">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="23731-130">Remove-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="23731-131">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="23731-131">Remove-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="23731-132">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="23731-132">Remove-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="23731-133">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="23731-133">Remove-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="23731-134">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="23731-134">Set-AzureKeyVaultCertificateAttribute</span></span>
    + <span data-ttu-id="23731-135">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="23731-135">Set-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="23731-136">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="23731-136">Set-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="23731-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="23731-137">Stop-AzureKeyVaultCertificateOperation</span></span>
* <span data-ttu-id="23731-138">Rete</span><span class="sxs-lookup"><span data-stu-id="23731-138">Network</span></span>

  - <span data-ttu-id="23731-139">Aggiunta di un nuovo parametro opzionale per l'interfaccia di rete per abilitare/disabilitare la rete accelerata +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="23731-139">New switch parameter added for network interface to enable/disable accelerated networking +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span></span>
  - <span data-ttu-id="23731-140">Abilitazione di cmdlet di PowerShell per la funzionalità del gateway attiva-attiva</span><span class="sxs-lookup"><span data-stu-id="23731-140">Enable Active-Active gateway feature PowerShell cmdlets</span></span>
    + <span data-ttu-id="23731-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="23731-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
    + <span data-ttu-id="23731-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="23731-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="23731-143">Aggiunta di un nuovo cmdlet</span><span class="sxs-lookup"><span data-stu-id="23731-143">Added new cmdlet</span></span>
    + <span data-ttu-id="23731-144">Test-AzureRmPrivateIpAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="23731-144">Test-AzureRmPrivateIpAddressAvailability</span></span>
* <span data-ttu-id="23731-145">Risorse</span><span class="sxs-lookup"><span data-stu-id="23731-145">Resources</span></span>
  - <span data-ttu-id="23731-146">Supporto delle zone nei cmdlet di provider e risorse</span><span class="sxs-lookup"><span data-stu-id="23731-146">Support zones in provider and resource cmdlets</span></span>
    + <span data-ttu-id="23731-147">Get-AzureRmProvider</span><span class="sxs-lookup"><span data-stu-id="23731-147">Get-AzureRmProvider</span></span>
    + <span data-ttu-id="23731-148">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="23731-148">New-AzureRmResource</span></span>
    + <span data-ttu-id="23731-149">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="23731-149">Set-AzureRmResource</span></span>
* <span data-ttu-id="23731-150">Sql</span><span class="sxs-lookup"><span data-stu-id="23731-150">Sql</span></span>
  - <span data-ttu-id="23731-151">Aggiunta di nuovi cmdlet per la gestione dei criteri di rilevamento delle minacce di SQL di Azure a livello di server</span><span class="sxs-lookup"><span data-stu-id="23731-151">Added new cmdlets for Azure SQL threat detection policy management at server level</span></span>
    + <span data-ttu-id="23731-152">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="23731-152">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="23731-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="23731-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="23731-154">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="23731-154">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
  - <span data-ttu-id="23731-155">Aggiunta di nuovi cmdlet per supportare l'abilitazione/disabilitazione di GeoBackupPolicy per Azure SQL Data Warehouse</span><span class="sxs-lookup"><span data-stu-id="23731-155">Added new cmdlets to support enabling/disabling GeoBackupPolicy for Sql Azure DataWarehouses</span></span>
    + <span data-ttu-id="23731-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="23731-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
    + <span data-ttu-id="23731-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="23731-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
  - <span data-ttu-id="23731-158">Aggiunta di nuovi cmdlet per Advisor SQL di Azure e API per azioni consigliate</span><span class="sxs-lookup"><span data-stu-id="23731-158">Added new cmdlets for Azure Sql Advisors and Recommended Actions APIs</span></span>
    + <span data-ttu-id="23731-159">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="23731-159">Get-AzureRmSqlDatabaseAdvisor</span></span>
    + <span data-ttu-id="23731-160">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="23731-160">Get-AzureRmSqlElasticPoolAdvisor</span></span>
    + <span data-ttu-id="23731-161">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="23731-161">Get-AzureRmSqlServerAdvisor</span></span>
    + <span data-ttu-id="23731-162">Get-AzureRmSqlDatabaseRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="23731-162">Get-AzureRmSqlDatabaseRecommendedActions</span></span>
    + <span data-ttu-id="23731-163">Get-AzureRmSqlElasticPoolRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="23731-163">Get-AzureRmSqlElasticPoolRecommendedActions</span></span>
    + <span data-ttu-id="23731-164">Get-AzureRmSqlServerRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="23731-164">Get-AzureRmSqlServerRecommendedActions</span></span>
    + <span data-ttu-id="23731-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="23731-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="23731-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="23731-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="23731-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="23731-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="23731-168">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="23731-168">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>
    + <span data-ttu-id="23731-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="23731-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>
    + <span data-ttu-id="23731-170">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="23731-170">Set-AzureRmSqlServerRecommendedActionState</span></span>
