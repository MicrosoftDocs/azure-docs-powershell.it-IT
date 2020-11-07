---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: b9b6092035d97aed8f70137c4157bfb80bf3f62a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677769"
---
# <span data-ttu-id="cd6dc-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="cd6dc-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="cd6dc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd6dc-102">SYNOPSIS</span></span>
<span data-ttu-id="cd6dc-103">Ottiene i tasti di scelta correnti associati a una raccolta di un'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="cd6dc-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="cd6dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd6dc-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd6dc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd6dc-105">DESCRIPTION</span></span>
<span data-ttu-id="cd6dc-106">Il cmdlet **Get-AzPowerBIWorkspaceCollectionAccessKey** ottiene i tasti di scelta correnti associati a una raccolta di un'area di lavoro di Power bi.</span><span class="sxs-lookup"><span data-stu-id="cd6dc-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="cd6dc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd6dc-107">EXAMPLES</span></span>

### <span data-ttu-id="cd6dc-108">Esempio 1: ottenere i tasti di scelta</span><span class="sxs-lookup"><span data-stu-id="cd6dc-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="cd6dc-109">Questo comando ottiene i tasti di scelta per la raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="cd6dc-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="cd6dc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd6dc-110">PARAMETERS</span></span>

### <span data-ttu-id="cd6dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd6dc-111">-DefaultProfile</span></span>
<span data-ttu-id="cd6dc-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cd6dc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd6dc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd6dc-113">-ResourceGroupName</span></span>
<span data-ttu-id="cd6dc-114">Specifica il nome del gruppo di risorse della raccolta.</span><span class="sxs-lookup"><span data-stu-id="cd6dc-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="cd6dc-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="cd6dc-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="cd6dc-116">Specifica il nome della raccolta dell'area di lavoro di Power BI in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd6dc-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cd6dc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd6dc-117">CommonParameters</span></span>
<span data-ttu-id="cd6dc-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd6dc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd6dc-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd6dc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd6dc-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd6dc-120">INPUTS</span></span>

### <span data-ttu-id="cd6dc-121">System. String</span><span class="sxs-lookup"><span data-stu-id="cd6dc-121">System.String</span></span>

## <span data-ttu-id="cd6dc-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd6dc-122">OUTPUTS</span></span>

### <span data-ttu-id="cd6dc-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="cd6dc-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="cd6dc-124">Note</span><span class="sxs-lookup"><span data-stu-id="cd6dc-124">NOTES</span></span>

## <span data-ttu-id="cd6dc-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd6dc-125">RELATED LINKS</span></span>

[<span data-ttu-id="cd6dc-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="cd6dc-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


