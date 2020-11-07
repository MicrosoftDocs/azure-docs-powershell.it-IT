---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9595E785-6DBF-433C-83B3-8506A3B49B13
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 242dfd46b179d1e7d55613d938eddf5b691da6c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687975"
---
# <span data-ttu-id="659bd-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="659bd-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="659bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="659bd-102">SYNOPSIS</span></span>
<span data-ttu-id="659bd-103">Ottiene il file di impostazioni del caveau di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="659bd-103">Gets the Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="659bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="659bd-104">SYNTAX</span></span>

### <span data-ttu-id="659bd-105">ByParam (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="659bd-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="659bd-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="659bd-106">Default</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="659bd-107">ForSite</span><span class="sxs-lookup"><span data-stu-id="659bd-107">ForSite</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> -SiteIdentifier <String> -SiteFriendlyName <String>
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="659bd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="659bd-108">DESCRIPTION</span></span>
<span data-ttu-id="659bd-109">Il cmdlet **Get-AzureRmSiteRecoveryVaultSettingsFile** ottiene il file di impostazioni per un Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="659bd-109">The **Get-AzureRmSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="659bd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="659bd-110">EXAMPLES</span></span>

## <span data-ttu-id="659bd-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="659bd-111">PARAMETERS</span></span>

### <span data-ttu-id="659bd-112">-Path</span><span class="sxs-lookup"><span data-stu-id="659bd-112">-Path</span></span>
<span data-ttu-id="659bd-113">Specifica il percorso del file di impostazioni del caveau di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="659bd-113">Specifies the path to the Site Recovery vault settings file.</span></span>
<span data-ttu-id="659bd-114">Per archiviare il file in locale, scaricarlo dal portale del Vault Recovery del sito una volta completato il comando.</span><span class="sxs-lookup"><span data-stu-id="659bd-114">To store this file locally, download it from the Site Recovery vault portal once the command completes.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, ForSite
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="659bd-115">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="659bd-115">-SiteFriendlyName</span></span>
<span data-ttu-id="659bd-116">Specifica il nome descrittivo del sito per il Vault quando il sito è un sito Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="659bd-116">Specifies the site friendly name for the vault when the site is a Hyper-V site.</span></span>

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

### <span data-ttu-id="659bd-117">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="659bd-117">-SiteIdentifier</span></span>
<span data-ttu-id="659bd-118">Specifica l'identificatore del sito per il Vault quando il sito è un sito Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="659bd-118">Specifies the site identifier for the vault when the site is a Hyper-V site.</span></span>

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

### <span data-ttu-id="659bd-119">-Vault</span><span class="sxs-lookup"><span data-stu-id="659bd-119">-Vault</span></span>
<span data-ttu-id="659bd-120">Specifica l'oggetto Vault per il sito.</span><span class="sxs-lookup"><span data-stu-id="659bd-120">Specifies the vault object for the site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: Default, ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="659bd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="659bd-121">-DefaultProfile</span></span>
<span data-ttu-id="659bd-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="659bd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="659bd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="659bd-123">CommonParameters</span></span>
<span data-ttu-id="659bd-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="659bd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="659bd-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="659bd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="659bd-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="659bd-126">INPUTS</span></span>

### <span data-ttu-id="659bd-127">ASRVault</span><span class="sxs-lookup"><span data-stu-id="659bd-127">ASRVault</span></span>
<span data-ttu-id="659bd-128">Il parametro "Vault" accetta il valore di tipo "ASRVault" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="659bd-128">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="659bd-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="659bd-129">OUTPUTS</span></span>

### <span data-ttu-id="659bd-130">Microsoft. Azure. Commands. SiteRecovery. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="659bd-130">Microsoft.Azure.Commands.SiteRecovery.VaultSettingsFilePath</span></span>

## <span data-ttu-id="659bd-131">Note</span><span class="sxs-lookup"><span data-stu-id="659bd-131">NOTES</span></span>

## <span data-ttu-id="659bd-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="659bd-132">RELATED LINKS</span></span>

[<span data-ttu-id="659bd-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="659bd-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureRmSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="659bd-134">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="659bd-134">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)
