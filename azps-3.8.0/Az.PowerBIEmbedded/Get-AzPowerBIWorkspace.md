---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 06cbaf240214bb61fb6bceac2827b9ce04d956f4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018626"
---
# <span data-ttu-id="4935a-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="4935a-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="4935a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4935a-102">SYNOPSIS</span></span>
<span data-ttu-id="4935a-103">Ottiene le aree di lavoro in una raccolta di un'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="4935a-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="4935a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4935a-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4935a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4935a-105">DESCRIPTION</span></span>
<span data-ttu-id="4935a-106">Il cmdlet **Get-AzPowerBIWorkspace** ottiene le aree di lavoro in una raccolta di un'area di lavoro di Power bi.</span><span class="sxs-lookup"><span data-stu-id="4935a-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="4935a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4935a-107">EXAMPLES</span></span>

### <span data-ttu-id="4935a-108">Esempio 1: recuperare le aree di lavoro di una raccolta di area di lavoro</span><span class="sxs-lookup"><span data-stu-id="4935a-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="4935a-109">Questo comando consente di ottenere le aree di lavoro che appartengono alla raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="4935a-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="4935a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4935a-110">PARAMETERS</span></span>

### <span data-ttu-id="4935a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4935a-111">-DefaultProfile</span></span>
<span data-ttu-id="4935a-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4935a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4935a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4935a-113">-ResourceGroupName</span></span>
<span data-ttu-id="4935a-114">Specifica il nome del gruppo di risorse a cui appartiene la raccolta dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="4935a-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="4935a-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="4935a-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="4935a-116">Specifica il nome della raccolta dell'area di lavoro per cui questo cmdlet ottiene le aree di lavoro.</span><span class="sxs-lookup"><span data-stu-id="4935a-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="4935a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4935a-117">CommonParameters</span></span>
<span data-ttu-id="4935a-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4935a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4935a-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4935a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4935a-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4935a-120">INPUTS</span></span>

### <span data-ttu-id="4935a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="4935a-121">System.String</span></span>

## <span data-ttu-id="4935a-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4935a-122">OUTPUTS</span></span>

### <span data-ttu-id="4935a-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="4935a-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="4935a-124">Note</span><span class="sxs-lookup"><span data-stu-id="4935a-124">NOTES</span></span>

## <span data-ttu-id="4935a-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4935a-125">RELATED LINKS</span></span>

[<span data-ttu-id="4935a-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="4935a-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


