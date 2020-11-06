---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 603cd65195f9e33c5006dcb4f2dc98ffc64aa7a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519989"
---
# <span data-ttu-id="289ad-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="289ad-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="289ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="289ad-102">SYNOPSIS</span></span>
<span data-ttu-id="289ad-103">Ottiene il file di impostazioni del Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="289ad-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="289ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="289ad-104">SYNTAX</span></span>

### <span data-ttu-id="289ad-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="289ad-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="289ad-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="289ad-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="289ad-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="289ad-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="289ad-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="289ad-108">DESCRIPTION</span></span>
<span data-ttu-id="289ad-109">Il cmdlet **Get-AzureRmRecoveryServicesVaultSettingsFile** ottiene il file di impostazioni per un Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="289ad-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="289ad-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="289ad-110">EXAMPLES</span></span>

### <span data-ttu-id="289ad-111">Esempio 1: registrare un computer Windows Server o DPM per Azure Backup</span><span class="sxs-lookup"><span data-stu-id="289ad-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="289ad-112">Il primo comando ottiene il Vault denominato TestVault e lo archivia nella variabile $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="289ad-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="289ad-113">Il secondo comando imposta la variabile $CredsPath su C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="289ad-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="289ad-114">L'ultimo comando ottiene il file delle credenziali del Vault per $Vault 01 usando le credenziali in $CredsPath per il backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="289ad-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

## <span data-ttu-id="289ad-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="289ad-115">PARAMETERS</span></span>

### <span data-ttu-id="289ad-116">-Backup</span><span class="sxs-lookup"><span data-stu-id="289ad-116">-Backup</span></span>
<span data-ttu-id="289ad-117">Indica che il file delle credenziali del Vault è applicabile a Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="289ad-117">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289ad-118">-Path</span><span class="sxs-lookup"><span data-stu-id="289ad-118">-Path</span></span>
<span data-ttu-id="289ad-119">Specifica il percorso del file di impostazioni del Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="289ad-119">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="289ad-120">È possibile scaricare il file dal portale del Vault di ripristino di Azure sito e archiviarlo localmente.</span><span class="sxs-lookup"><span data-stu-id="289ad-120">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="289ad-121">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="289ad-121">-SiteFriendlyName</span></span>
<span data-ttu-id="289ad-122">Specifica il nome descrittivo del sito.</span><span class="sxs-lookup"><span data-stu-id="289ad-122">Specifies the site friendly name.</span></span>
<span data-ttu-id="289ad-123">Usare questo parametro se si scaricano le credenziali del Vault per un sito Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="289ad-123">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289ad-124">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="289ad-124">-SiteIdentifier</span></span>
<span data-ttu-id="289ad-125">Specifica l'identificatore del sito.</span><span class="sxs-lookup"><span data-stu-id="289ad-125">Specifies the site identifier.</span></span>
<span data-ttu-id="289ad-126">Usare questo parametro se si scaricano le credenziali del Vault per un sito Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="289ad-126">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289ad-127">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="289ad-127">-SiteRecovery</span></span>
<span data-ttu-id="289ad-128">Indica che il file delle credenziali del Vault è applicabile al ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="289ad-128">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289ad-129">-Vault</span><span class="sxs-lookup"><span data-stu-id="289ad-129">-Vault</span></span>
<span data-ttu-id="289ad-130">Specifica l'oggetto del Vault di ripristino di Azure sito.</span><span class="sxs-lookup"><span data-stu-id="289ad-130">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="289ad-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="289ad-131">-DefaultProfile</span></span>
<span data-ttu-id="289ad-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="289ad-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289ad-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="289ad-133">CommonParameters</span></span>
<span data-ttu-id="289ad-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="289ad-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="289ad-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="289ad-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="289ad-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="289ad-136">INPUTS</span></span>

### <span data-ttu-id="289ad-137">ARSVault</span><span class="sxs-lookup"><span data-stu-id="289ad-137">ARSVault</span></span>
<span data-ttu-id="289ad-138">Il parametro "Vault" accetta il valore di tipo "ARSVault" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="289ad-138">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="289ad-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="289ad-139">OUTPUTS</span></span>

### <span data-ttu-id="289ad-140">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="289ad-140">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="289ad-141">Note</span><span class="sxs-lookup"><span data-stu-id="289ad-141">NOTES</span></span>

## <span data-ttu-id="289ad-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="289ad-142">RELATED LINKS</span></span>

[<span data-ttu-id="289ad-143">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="289ad-143">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="289ad-144">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="289ad-144">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="289ad-145">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="289ad-145">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


