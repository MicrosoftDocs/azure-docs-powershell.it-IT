---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 143d92384fd270711378f6741ba59e88c12833d1
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a><span data-ttu-id="50b4f-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="50b4f-103">Release notes</span></span>

<span data-ttu-id="50b4f-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="50b4f-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-220"></a><span data-ttu-id="50b4f-105">Versione 2.2.0</span><span class="sxs-lookup"><span data-stu-id="50b4f-105">Version 2.2.0</span></span>
* <span data-ttu-id="50b4f-106">Calcolo</span><span class="sxs-lookup"><span data-stu-id="50b4f-106">Compute</span></span>
  - <span data-ttu-id="50b4f-107">Aggiunta del supporto per l'esecuzione di query sullo stato di crittografia dall'estensione AzureDiskEncryptionForLinux</span><span class="sxs-lookup"><span data-stu-id="50b4f-107">Add support for querying encryption status from the AzureDiskEncryptionForLinux extension</span></span>
* <span data-ttu-id="50b4f-108">DataFactory</span><span class="sxs-lookup"><span data-stu-id="50b4f-108">DataFactory</span></span>
  - <span data-ttu-id="50b4f-109">Aggiunta di un nuovo cmdlet per elencare le finestre attività</span><span class="sxs-lookup"><span data-stu-id="50b4f-109">Added new cmdlet for listing activity windows</span></span>
    + <span data-ttu-id="50b4f-110">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="50b4f-110">Get-AzureRmDataFactoryActivityWindow</span></span>
* <span data-ttu-id="50b4f-111">DataLake</span><span class="sxs-lookup"><span data-stu-id="50b4f-111">DataLake</span></span>
  - <span data-ttu-id="50b4f-112">Modifica del parametro `Host` in `DatabaseHost` e aggiunta dell'alias a `Host`</span><span class="sxs-lookup"><span data-stu-id="50b4f-112">Changed parameter `Host` to `DatabaseHost` and added alias to `Host`</span></span>
    + <span data-ttu-id="50b4f-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="50b4f-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
    + <span data-ttu-id="50b4f-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="50b4f-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
  - <span data-ttu-id="50b4f-115">Aggiunta del supporto per la rimozione di ACL e ACL predefiniti</span><span class="sxs-lookup"><span data-stu-id="50b4f-115">Add support for ACL and Default ACL removal</span></span>
  - <span data-ttu-id="50b4f-116">Aggiunta del supporto per ottenere e impostare autorizzazioni senza nome per file e cartelle</span><span class="sxs-lookup"><span data-stu-id="50b4f-116">Add support for getting and setting unnamed permissions on files and folders</span></span>
* <span data-ttu-id="50b4f-117">Insieme di credenziali delle chiavi</span><span class="sxs-lookup"><span data-stu-id="50b4f-117">KeyVault</span></span>
  - <span data-ttu-id="50b4f-118">Aggiunta del supporto per certificati</span><span class="sxs-lookup"><span data-stu-id="50b4f-118">Add support for certificates</span></span>
    + <span data-ttu-id="50b4f-119">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="50b4f-119">Add-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="50b4f-120">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="50b4f-120">Add-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="50b4f-121">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="50b4f-121">Get-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="50b4f-122">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="50b4f-122">Get-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="50b4f-123">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="50b4f-123">Get-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="50b4f-124">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="50b4f-124">Get-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="50b4f-125">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="50b4f-125">Get-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="50b4f-126">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="50b4f-126">Import-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="50b4f-127">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="50b4f-127">New-AzureKeyVaultCertificateAdministratorDetails</span></span>
    + <span data-ttu-id="50b4f-128">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="50b4f-128">New-AzureKeyVaultCertificateOrganizationDetails</span></span>
    + <span data-ttu-id="50b4f-129">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="50b4f-129">New-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="50b4f-130">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="50b4f-130">Remove-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="50b4f-131">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="50b4f-131">Remove-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="50b4f-132">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="50b4f-132">Remove-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="50b4f-133">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="50b4f-133">Remove-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="50b4f-134">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="50b4f-134">Set-AzureKeyVaultCertificateAttribute</span></span>
    + <span data-ttu-id="50b4f-135">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="50b4f-135">Set-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="50b4f-136">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="50b4f-136">Set-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="50b4f-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="50b4f-137">Stop-AzureKeyVaultCertificateOperation</span></span>
* <span data-ttu-id="50b4f-138">Rete</span><span class="sxs-lookup"><span data-stu-id="50b4f-138">Network</span></span>

  - <span data-ttu-id="50b4f-139">Aggiunta di un nuovo parametro opzionale per l'interfaccia di rete per abilitare/disabilitare la rete accelerata +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="50b4f-139">New switch parameter added for network interface to enable/disable accelerated networking +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span></span>
  - <span data-ttu-id="50b4f-140">Abilitazione di cmdlet di PowerShell per la funzionalità del gateway attiva-attiva</span><span class="sxs-lookup"><span data-stu-id="50b4f-140">Enable Active-Active gateway feature PowerShell cmdlets</span></span>
    + <span data-ttu-id="50b4f-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="50b4f-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
    + <span data-ttu-id="50b4f-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="50b4f-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="50b4f-143">Aggiunta di un nuovo cmdlet</span><span class="sxs-lookup"><span data-stu-id="50b4f-143">Added new cmdlet</span></span>
    + <span data-ttu-id="50b4f-144">Test-AzureRmPrivateIpAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="50b4f-144">Test-AzureRmPrivateIpAddressAvailability</span></span>
* <span data-ttu-id="50b4f-145">Risorse</span><span class="sxs-lookup"><span data-stu-id="50b4f-145">Resources</span></span>
  - <span data-ttu-id="50b4f-146">Supporto delle zone nei cmdlet di provider e risorse</span><span class="sxs-lookup"><span data-stu-id="50b4f-146">Support zones in provider and resource cmdlets</span></span>
    + <span data-ttu-id="50b4f-147">Get-AzureRmProvider</span><span class="sxs-lookup"><span data-stu-id="50b4f-147">Get-AzureRmProvider</span></span>
    + <span data-ttu-id="50b4f-148">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="50b4f-148">New-AzureRmResource</span></span>
    + <span data-ttu-id="50b4f-149">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="50b4f-149">Set-AzureRmResource</span></span>
* <span data-ttu-id="50b4f-150">Sql</span><span class="sxs-lookup"><span data-stu-id="50b4f-150">Sql</span></span>
  - <span data-ttu-id="50b4f-151">Aggiunta di nuovi cmdlet per la gestione dei criteri di rilevamento delle minacce di SQL di Azure a livello di server</span><span class="sxs-lookup"><span data-stu-id="50b4f-151">Added new cmdlets for Azure SQL threat detection policy management at server level</span></span>
    + <span data-ttu-id="50b4f-152">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="50b4f-152">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="50b4f-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="50b4f-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="50b4f-154">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="50b4f-154">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
  - <span data-ttu-id="50b4f-155">Aggiunta di nuovi cmdlet per supportare l'abilitazione/disabilitazione di GeoBackupPolicy per Azure SQL Data Warehouse</span><span class="sxs-lookup"><span data-stu-id="50b4f-155">Added new cmdlets to support enabling/disabling GeoBackupPolicy for Sql Azure DataWarehouses</span></span>
    + <span data-ttu-id="50b4f-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="50b4f-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
    + <span data-ttu-id="50b4f-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="50b4f-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
  - <span data-ttu-id="50b4f-158">Aggiunta di nuovi cmdlet per Advisor SQL di Azure e API per azioni consigliate</span><span class="sxs-lookup"><span data-stu-id="50b4f-158">Added new cmdlets for Azure Sql Advisors and Recommended Actions APIs</span></span>
    + <span data-ttu-id="50b4f-159">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="50b4f-159">Get-AzureRmSqlDatabaseAdvisor</span></span>
    + <span data-ttu-id="50b4f-160">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="50b4f-160">Get-AzureRmSqlElasticPoolAdvisor</span></span>
    + <span data-ttu-id="50b4f-161">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="50b4f-161">Get-AzureRmSqlServerAdvisor</span></span>
    + <span data-ttu-id="50b4f-162">Get-AzureRmSqlDatabaseRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="50b4f-162">Get-AzureRmSqlDatabaseRecommendedActions</span></span>
    + <span data-ttu-id="50b4f-163">Get-AzureRmSqlElasticPoolRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="50b4f-163">Get-AzureRmSqlElasticPoolRecommendedActions</span></span>
    + <span data-ttu-id="50b4f-164">Get-AzureRmSqlServerRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="50b4f-164">Get-AzureRmSqlServerRecommendedActions</span></span>
    + <span data-ttu-id="50b4f-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="50b4f-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="50b4f-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="50b4f-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="50b4f-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="50b4f-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="50b4f-168">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="50b4f-168">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>
    + <span data-ttu-id="50b4f-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="50b4f-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>
    + <span data-ttu-id="50b4f-170">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="50b4f-170">Set-AzureRmSqlServerRecommendedActionState</span></span>
