---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 9108f224297b23fd391e1a4c3afac4b826aa3dbf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355771"
---
# <span data-ttu-id="b7c73-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="b7c73-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="b7c73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7c73-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c73-103">Ottiene i tasti di scelta correnti associati a una raccolta di un'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="b7c73-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="b7c73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7c73-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7c73-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7c73-105">DESCRIPTION</span></span>
<span data-ttu-id="b7c73-106">Il cmdlet **Get-AzPowerBIWorkspaceCollectionAccessKey** ottiene i tasti di scelta correnti associati a una raccolta di un'area di lavoro di Power bi.</span><span class="sxs-lookup"><span data-stu-id="b7c73-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="b7c73-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7c73-107">EXAMPLES</span></span>

### <span data-ttu-id="b7c73-108">Esempio 1: ottenere i tasti di scelta</span><span class="sxs-lookup"><span data-stu-id="b7c73-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="b7c73-109">Questo comando ottiene i tasti di scelta per la raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b7c73-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="b7c73-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7c73-110">PARAMETERS</span></span>

### <span data-ttu-id="b7c73-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c73-111">-DefaultProfile</span></span>
<span data-ttu-id="b7c73-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b7c73-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7c73-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c73-113">-ResourceGroupName</span></span>
<span data-ttu-id="b7c73-114">Specifica il nome del gruppo di risorse della raccolta.</span><span class="sxs-lookup"><span data-stu-id="b7c73-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="b7c73-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="b7c73-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="b7c73-116">Specifica il nome della raccolta dell'area di lavoro di Power BI in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7c73-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b7c73-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c73-117">CommonParameters</span></span>
<span data-ttu-id="b7c73-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c73-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c73-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7c73-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c73-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7c73-120">INPUTS</span></span>

### <span data-ttu-id="b7c73-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b7c73-121">System.String</span></span>

## <span data-ttu-id="b7c73-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7c73-122">OUTPUTS</span></span>

### <span data-ttu-id="b7c73-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="b7c73-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="b7c73-124">Note</span><span class="sxs-lookup"><span data-stu-id="b7c73-124">NOTES</span></span>

## <span data-ttu-id="b7c73-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7c73-125">RELATED LINKS</span></span>

[<span data-ttu-id="b7c73-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="b7c73-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


