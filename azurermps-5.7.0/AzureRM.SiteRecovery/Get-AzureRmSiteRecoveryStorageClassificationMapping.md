---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D19488C1-9E87-4F1A-94E3-8AFDE6AFC982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: e04f5b71fe0cc5d6872c3bdf9cd18790f4e09f7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687435"
---
# <span data-ttu-id="7d81d-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="7d81d-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="7d81d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d81d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d81d-103">Ottiene un mapping di classificazione dello spazio di archiviazione nel ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="7d81d-103">Gets a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d81d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d81d-104">SYNTAX</span></span>

### <span data-ttu-id="7d81d-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d81d-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d81d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7d81d-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d81d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d81d-107">DESCRIPTION</span></span>
<span data-ttu-id="7d81d-108">Il cmdlet **Get-AzureRmSiteRecoveryStorageClassificationMapping** ottiene un mapping di classificazione dello spazio di archiviazione nel ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d81d-108">The **Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet gets a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="7d81d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d81d-109">EXAMPLES</span></span>

## <span data-ttu-id="7d81d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d81d-110">PARAMETERS</span></span>

### <span data-ttu-id="7d81d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d81d-111">-DefaultProfile</span></span>
<span data-ttu-id="7d81d-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d81d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d81d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d81d-113">-Name</span></span>
<span data-ttu-id="7d81d-114">Specifica il nome del mapping di classificazione dello spazio di archiviazione ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d81d-114">Specifies the name of the storage classification mapping that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d81d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d81d-115">CommonParameters</span></span>
<span data-ttu-id="7d81d-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d81d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d81d-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d81d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d81d-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d81d-118">INPUTS</span></span>

### <span data-ttu-id="7d81d-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7d81d-119">None</span></span>
<span data-ttu-id="7d81d-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7d81d-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7d81d-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d81d-121">OUTPUTS</span></span>

### <span data-ttu-id="7d81d-122">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRStorageClassificationMapping]</span><span class="sxs-lookup"><span data-stu-id="7d81d-122">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping]</span></span>

## <span data-ttu-id="7d81d-123">Note</span><span class="sxs-lookup"><span data-stu-id="7d81d-123">NOTES</span></span>

## <span data-ttu-id="7d81d-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d81d-124">RELATED LINKS</span></span>

[<span data-ttu-id="7d81d-125">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="7d81d-125">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="7d81d-126">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="7d81d-126">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
