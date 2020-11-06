---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F3E1BEB5-B565-4618-9AEF-DB85A1AB2163
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 31887397c6b9b0a3a18a4af3cb4b4faca7c4a91a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520365"
---
# <span data-ttu-id="58030-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="58030-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="58030-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58030-102">SYNOPSIS</span></span>
<span data-ttu-id="58030-103">Ottiene i mapping del contenitore di protezione del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="58030-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58030-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58030-104">SYNTAX</span></span>

### <span data-ttu-id="58030-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58030-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58030-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="58030-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58030-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58030-107">DESCRIPTION</span></span>
<span data-ttu-id="58030-108">Il cmdlet **Get-AzureRmSiteRecoveryProtectionContainerMapping** ottiene le informazioni sul contenitore di protezione per i mapping dei criteri nel Vault.</span><span class="sxs-lookup"><span data-stu-id="58030-108">The **Get-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet gets information about the Protection Container to Policy mappings in the vault.</span></span>

## <span data-ttu-id="58030-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58030-109">EXAMPLES</span></span>

## <span data-ttu-id="58030-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58030-110">PARAMETERS</span></span>

### <span data-ttu-id="58030-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58030-111">-DefaultProfile</span></span>
<span data-ttu-id="58030-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58030-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58030-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="58030-113">-Name</span></span>
<span data-ttu-id="58030-114">Specifica il nome del mapping del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="58030-114">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58030-115">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="58030-115">-ProtectionContainer</span></span>
<span data-ttu-id="58030-116">Specifica l'oggetto contenitore di protezione per il ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="58030-116">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58030-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58030-117">CommonParameters</span></span>
<span data-ttu-id="58030-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58030-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58030-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58030-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58030-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58030-120">INPUTS</span></span>

### <span data-ttu-id="58030-121">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="58030-121">ASRProtectionContainer</span></span>
<span data-ttu-id="58030-122">Il parametro ' ProtectionContainer ' accetta il valore di tipo ' ASRProtectionContainer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="58030-122">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="58030-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58030-123">OUTPUTS</span></span>

### <span data-ttu-id="58030-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="58030-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="58030-125">Note</span><span class="sxs-lookup"><span data-stu-id="58030-125">NOTES</span></span>

## <span data-ttu-id="58030-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58030-126">RELATED LINKS</span></span>

[<span data-ttu-id="58030-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="58030-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="58030-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="58030-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
