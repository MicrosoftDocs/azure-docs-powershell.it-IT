---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: b272f22c0bac37f5318deff50f1f0b56a849ce2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687020"
---
# <span data-ttu-id="decb1-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="decb1-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="decb1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="decb1-102">SYNOPSIS</span></span>
<span data-ttu-id="decb1-103">Ottiene il file di impostazioni del Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="decb1-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="decb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="decb1-104">SYNTAX</span></span>

### <span data-ttu-id="decb1-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="decb1-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="decb1-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="decb1-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="decb1-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="decb1-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="decb1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="decb1-108">DESCRIPTION</span></span>
<span data-ttu-id="decb1-109">Il cmdlet **Get-AzureRmRecoveryServicesVaultSettingsFile** ottiene il file di impostazioni per un Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="decb1-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="decb1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="decb1-110">EXAMPLES</span></span>

### <span data-ttu-id="decb1-111">Esempio 1: registrare un computer Windows Server o DPM per Azure Backup</span><span class="sxs-lookup"><span data-stu-id="decb1-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="decb1-112">Il primo comando ottiene il Vault denominato TestVault e lo archivia nella variabile $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="decb1-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="decb1-113">Il secondo comando imposta la variabile $CredsPath su C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="decb1-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="decb1-114">L'ultimo comando ottiene il file delle credenziali del Vault per $Vault 01 usando le credenziali in $CredsPath per il backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="decb1-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="decb1-115">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="decb1-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="decb1-116">Il comando ottiene il file delle credenziali del Vault per $Vault 01 di tipo Vault siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="decb1-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="decb1-117">Esempio 3: registrare un computer Windows Server o DPM per Azure Backup</span><span class="sxs-lookup"><span data-stu-id="decb1-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="decb1-118">Il comando ottiene il file delle credenziali del Vault per $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="decb1-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="decb1-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="decb1-119">PARAMETERS</span></span>

### <span data-ttu-id="decb1-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="decb1-120">-Backup</span></span>
<span data-ttu-id="decb1-121">Indica che il file delle credenziali del Vault è applicabile a Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="decb1-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decb1-122">-Path</span><span class="sxs-lookup"><span data-stu-id="decb1-122">-Path</span></span>
<span data-ttu-id="decb1-123">Specifica il percorso del file di impostazioni del Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="decb1-123">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="decb1-124">È possibile scaricare il file dal portale del Vault di ripristino di Azure sito e archiviarlo localmente.</span><span class="sxs-lookup"><span data-stu-id="decb1-124">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decb1-125">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="decb1-125">-SiteFriendlyName</span></span>
<span data-ttu-id="decb1-126">Specifica il nome descrittivo del sito.</span><span class="sxs-lookup"><span data-stu-id="decb1-126">Specifies the site friendly name.</span></span>
<span data-ttu-id="decb1-127">Usare questo parametro se si scaricano le credenziali del Vault per un sito Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="decb1-127">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decb1-128">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="decb1-128">-SiteIdentifier</span></span>
<span data-ttu-id="decb1-129">Specifica l'identificatore del sito.</span><span class="sxs-lookup"><span data-stu-id="decb1-129">Specifies the site identifier.</span></span>
<span data-ttu-id="decb1-130">Usare questo parametro se si scaricano le credenziali del Vault per un sito Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="decb1-130">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decb1-131">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="decb1-131">-SiteRecovery</span></span>
<span data-ttu-id="decb1-132">Indica che il file delle credenziali del Vault è applicabile al ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="decb1-132">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decb1-133">-Vault</span><span class="sxs-lookup"><span data-stu-id="decb1-133">-Vault</span></span>
<span data-ttu-id="decb1-134">Specifica l'oggetto del Vault di ripristino di Azure sito.</span><span class="sxs-lookup"><span data-stu-id="decb1-134">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="decb1-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="decb1-135">-DefaultProfile</span></span>
<span data-ttu-id="decb1-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="decb1-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decb1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="decb1-137">CommonParameters</span></span>
<span data-ttu-id="decb1-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="decb1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="decb1-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="decb1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="decb1-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="decb1-140">INPUTS</span></span>

### <span data-ttu-id="decb1-141">ARSVault</span><span class="sxs-lookup"><span data-stu-id="decb1-141">ARSVault</span></span>
<span data-ttu-id="decb1-142">Il parametro "Vault" accetta il valore di tipo "ARSVault" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="decb1-142">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="decb1-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="decb1-143">OUTPUTS</span></span>

### <span data-ttu-id="decb1-144">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="decb1-144">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="decb1-145">Note</span><span class="sxs-lookup"><span data-stu-id="decb1-145">NOTES</span></span>

## <span data-ttu-id="decb1-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="decb1-146">RELATED LINKS</span></span>

[<span data-ttu-id="decb1-147">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="decb1-147">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="decb1-148">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="decb1-148">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="decb1-149">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="decb1-149">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


