---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 11c1e3c19a6f5767fcfe1120cfa3561a73885f5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511000"
---
# <span data-ttu-id="882d2-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="882d2-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="882d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="882d2-102">SYNOPSIS</span></span>
<span data-ttu-id="882d2-103">Ottiene i tasti di scelta correnti associati a una raccolta di un'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="882d2-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="882d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="882d2-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="882d2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="882d2-105">DESCRIPTION</span></span>
<span data-ttu-id="882d2-106">Il cmdlet **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** ottiene i tasti di scelta correnti associati a una raccolta di un'area di lavoro di Power bi.</span><span class="sxs-lookup"><span data-stu-id="882d2-106">The **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="882d2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="882d2-107">EXAMPLES</span></span>

### <span data-ttu-id="882d2-108">Esempio 1: ottenere i tasti di scelta</span><span class="sxs-lookup"><span data-stu-id="882d2-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="882d2-109">Questo comando ottiene i tasti di scelta per la raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="882d2-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="882d2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="882d2-110">PARAMETERS</span></span>

### <span data-ttu-id="882d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="882d2-111">-DefaultProfile</span></span>
<span data-ttu-id="882d2-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="882d2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="882d2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="882d2-113">-ResourceGroupName</span></span>
<span data-ttu-id="882d2-114">Specifica il nome del gruppo di risorse della raccolta.</span><span class="sxs-lookup"><span data-stu-id="882d2-114">Specifies the name of the resource group of the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="882d2-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="882d2-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="882d2-116">Specifica il nome della raccolta dell'area di lavoro di Power BI in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="882d2-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="882d2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="882d2-117">CommonParameters</span></span>
<span data-ttu-id="882d2-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="882d2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="882d2-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="882d2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="882d2-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="882d2-120">INPUTS</span></span>

### <span data-ttu-id="882d2-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="882d2-121">None</span></span>
<span data-ttu-id="882d2-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="882d2-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="882d2-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="882d2-123">OUTPUTS</span></span>

### <span data-ttu-id="882d2-124">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="882d2-124">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="882d2-125">Note</span><span class="sxs-lookup"><span data-stu-id="882d2-125">NOTES</span></span>

## <span data-ttu-id="882d2-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="882d2-126">RELATED LINKS</span></span>

[<span data-ttu-id="882d2-127">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="882d2-127">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


