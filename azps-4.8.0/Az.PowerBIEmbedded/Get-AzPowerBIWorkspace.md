---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 06cbaf240214bb61fb6bceac2827b9ce04d956f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189917"
---
# <span data-ttu-id="b4330-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="b4330-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="b4330-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4330-102">SYNOPSIS</span></span>
<span data-ttu-id="b4330-103">Ottiene le aree di lavoro in una raccolta di un'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="b4330-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="b4330-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4330-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4330-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4330-105">DESCRIPTION</span></span>
<span data-ttu-id="b4330-106">Il cmdlet **Get-AzPowerBIWorkspace** ottiene le aree di lavoro in una raccolta di un'area di lavoro di Power bi.</span><span class="sxs-lookup"><span data-stu-id="b4330-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="b4330-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4330-107">EXAMPLES</span></span>

### <span data-ttu-id="b4330-108">Esempio 1: recuperare le aree di lavoro di una raccolta di area di lavoro</span><span class="sxs-lookup"><span data-stu-id="b4330-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="b4330-109">Questo comando consente di ottenere le aree di lavoro che appartengono alla raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b4330-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="b4330-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4330-110">PARAMETERS</span></span>

### <span data-ttu-id="b4330-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4330-111">-DefaultProfile</span></span>
<span data-ttu-id="b4330-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b4330-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4330-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4330-113">-ResourceGroupName</span></span>
<span data-ttu-id="b4330-114">Specifica il nome del gruppo di risorse a cui appartiene la raccolta dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b4330-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="b4330-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="b4330-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="b4330-116">Specifica il nome della raccolta dell'area di lavoro per cui questo cmdlet ottiene le aree di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b4330-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="b4330-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4330-117">CommonParameters</span></span>
<span data-ttu-id="b4330-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4330-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4330-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4330-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4330-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4330-120">INPUTS</span></span>

### <span data-ttu-id="b4330-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b4330-121">System.String</span></span>

## <span data-ttu-id="b4330-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4330-122">OUTPUTS</span></span>

### <span data-ttu-id="b4330-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b4330-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="b4330-124">Note</span><span class="sxs-lookup"><span data-stu-id="b4330-124">NOTES</span></span>

## <span data-ttu-id="b4330-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4330-125">RELATED LINKS</span></span>

[<span data-ttu-id="b4330-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="b4330-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

