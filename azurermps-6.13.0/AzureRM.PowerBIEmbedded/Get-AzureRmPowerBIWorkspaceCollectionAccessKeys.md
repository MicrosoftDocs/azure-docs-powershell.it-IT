---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 61d71bebfd395b6856c93e0bc3642125437b5fe7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514960"
---
# <span data-ttu-id="c3014-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="c3014-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="c3014-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3014-102">SYNOPSIS</span></span>
<span data-ttu-id="c3014-103">Ottiene i tasti di scelta correnti associati a una raccolta di un'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="c3014-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3014-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3014-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3014-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3014-105">DESCRIPTION</span></span>
<span data-ttu-id="c3014-106">Il cmdlet **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** ottiene i tasti di scelta correnti associati a una raccolta di un'area di lavoro di Power bi.</span><span class="sxs-lookup"><span data-stu-id="c3014-106">The **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="c3014-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3014-107">EXAMPLES</span></span>

### <span data-ttu-id="c3014-108">Esempio 1: ottenere i tasti di scelta</span><span class="sxs-lookup"><span data-stu-id="c3014-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="c3014-109">Questo comando ottiene i tasti di scelta per la raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="c3014-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="c3014-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3014-110">PARAMETERS</span></span>

### <span data-ttu-id="c3014-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3014-111">-DefaultProfile</span></span>
<span data-ttu-id="c3014-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c3014-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3014-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3014-113">-ResourceGroupName</span></span>
<span data-ttu-id="c3014-114">Specifica il nome del gruppo di risorse della raccolta.</span><span class="sxs-lookup"><span data-stu-id="c3014-114">Specifies the name of the resource group of the collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3014-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="c3014-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="c3014-116">Specifica il nome della raccolta dell'area di lavoro di Power BI in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3014-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3014-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3014-117">CommonParameters</span></span>
<span data-ttu-id="c3014-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3014-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3014-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3014-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3014-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3014-120">INPUTS</span></span>

### <span data-ttu-id="c3014-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c3014-121">System.String</span></span>

## <span data-ttu-id="c3014-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3014-122">OUTPUTS</span></span>

### <span data-ttu-id="c3014-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="c3014-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="c3014-124">Note</span><span class="sxs-lookup"><span data-stu-id="c3014-124">NOTES</span></span>

## <span data-ttu-id="c3014-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3014-125">RELATED LINKS</span></span>

[<span data-ttu-id="c3014-126">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="c3014-126">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


