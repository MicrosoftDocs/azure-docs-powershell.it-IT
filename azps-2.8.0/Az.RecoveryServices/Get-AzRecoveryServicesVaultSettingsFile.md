---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 5455babba58e050397066e5439b3e046315b4101
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855682"
---
# <span data-ttu-id="d3d59-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d3d59-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="d3d59-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3d59-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d59-103">Ottiene il file di impostazioni del Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="d3d59-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="d3d59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3d59-104">SYNTAX</span></span>

### <span data-ttu-id="d3d59-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="d3d59-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3d59-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="d3d59-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3d59-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="d3d59-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3d59-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3d59-108">DESCRIPTION</span></span>
<span data-ttu-id="d3d59-109">Il cmdlet **Get-AzRecoveryServicesVaultSettingsFile** ottiene il file di impostazioni per un Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="d3d59-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d3d59-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3d59-110">EXAMPLES</span></span>

### <span data-ttu-id="d3d59-111">Esempio 1: registrare un computer Windows Server o DPM per Azure Backup</span><span class="sxs-lookup"><span data-stu-id="d3d59-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="d3d59-112">Il primo comando ottiene il Vault denominato TestVault e lo archivia nella variabile $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="d3d59-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="d3d59-113">Il secondo comando imposta la variabile $CredsPath su C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="d3d59-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="d3d59-114">L'ultimo comando ottiene il file delle credenziali del Vault per $Vault 01 usando le credenziali in $CredsPath per il backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d59-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="d3d59-115">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="d3d59-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="d3d59-116">Il comando ottiene il file delle credenziali del Vault per $Vault 01 di tipo Vault siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="d3d59-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="d3d59-117">Esempio 3: registrare un computer Windows Server o DPM per Azure Backup</span><span class="sxs-lookup"><span data-stu-id="d3d59-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="d3d59-118">Il comando ottiene il file delle credenziali del Vault per $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="d3d59-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="d3d59-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3d59-119">PARAMETERS</span></span>

### <span data-ttu-id="d3d59-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="d3d59-120">-Backup</span></span>
<span data-ttu-id="d3d59-121">Indica che il file delle credenziali del Vault è applicabile a Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="d3d59-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultTypeWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d59-122">-Certificato</span><span class="sxs-lookup"><span data-stu-id="d3d59-122">-Certificate</span></span>
<span data-ttu-id="d3d59-123">{{Fill certificate Description}}</span><span class="sxs-lookup"><span data-stu-id="d3d59-123">{{Fill Certificate Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d59-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d59-124">-DefaultProfile</span></span>
<span data-ttu-id="d3d59-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d59-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d59-126">-Path</span><span class="sxs-lookup"><span data-stu-id="d3d59-126">-Path</span></span>
<span data-ttu-id="d3d59-127">Specifica il percorso del file di impostazioni del Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="d3d59-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="d3d59-128">È possibile scaricare il file dal portale del Vault di ripristino di Azure sito e archiviarlo localmente.</span><span class="sxs-lookup"><span data-stu-id="d3d59-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d59-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d3d59-129">-SiteFriendlyName</span></span>
<span data-ttu-id="d3d59-130">Specifica il nome descrittivo del sito.</span><span class="sxs-lookup"><span data-stu-id="d3d59-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="d3d59-131">Usare questo parametro se si scaricano le credenziali del Vault per un sito Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="d3d59-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d59-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="d3d59-132">-SiteIdentifier</span></span>
<span data-ttu-id="d3d59-133">Specifica l'identificatore del sito.</span><span class="sxs-lookup"><span data-stu-id="d3d59-133">Specifies the site identifier.</span></span>
<span data-ttu-id="d3d59-134">Usare questo parametro se si scaricano le credenziali del Vault per un sito Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="d3d59-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d59-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d3d59-135">-SiteRecovery</span></span>
<span data-ttu-id="d3d59-136">Indica che il file delle credenziali del Vault è applicabile al ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d59-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSiteWithCertificate, ByDefaultWithCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d59-137">-Vault</span><span class="sxs-lookup"><span data-stu-id="d3d59-137">-Vault</span></span>
<span data-ttu-id="d3d59-138">Specifica l'oggetto del Vault di ripristino di Azure sito.</span><span class="sxs-lookup"><span data-stu-id="d3d59-138">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3d59-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d59-139">CommonParameters</span></span>
<span data-ttu-id="d3d59-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3d59-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d59-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3d59-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d59-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3d59-142">INPUTS</span></span>

### <span data-ttu-id="d3d59-143">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="d3d59-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="d3d59-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3d59-144">OUTPUTS</span></span>

### <span data-ttu-id="d3d59-145">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="d3d59-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="d3d59-146">Note</span><span class="sxs-lookup"><span data-stu-id="d3d59-146">NOTES</span></span>

## <span data-ttu-id="d3d59-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3d59-147">RELATED LINKS</span></span>

[<span data-ttu-id="d3d59-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d3d59-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="d3d59-149">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d3d59-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="d3d59-150">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d3d59-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


