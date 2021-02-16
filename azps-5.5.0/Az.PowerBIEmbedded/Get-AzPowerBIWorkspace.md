---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 06cbaf240214bb61fb6bceac2827b9ce04d956f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179071"
---
# <span data-ttu-id="0e756-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="0e756-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="0e756-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e756-102">SYNOPSIS</span></span>
<span data-ttu-id="0e756-103">Recupera le aree di lavoro in una raccolta di aree di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="0e756-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="0e756-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e756-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e756-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0e756-105">DESCRIPTION</span></span>
<span data-ttu-id="0e756-106">Il cmdlet **Get-AzPowerBIWorkspace ottiene** le aree di lavoro in una raccolta di aree di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="0e756-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="0e756-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e756-107">EXAMPLES</span></span>

### <span data-ttu-id="0e756-108">Esempio 1: Ottenere le aree di lavoro di una raccolta di aree di lavoro</span><span class="sxs-lookup"><span data-stu-id="0e756-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="0e756-109">Questo comando recupera le aree di lavoro che appartengono alla raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="0e756-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="0e756-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e756-110">PARAMETERS</span></span>

### <span data-ttu-id="0e756-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e756-111">-DefaultProfile</span></span>
<span data-ttu-id="0e756-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="0e756-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e756-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e756-113">-ResourceGroupName</span></span>
<span data-ttu-id="0e756-114">Specifica il nome del gruppo di risorse a cui appartiene la raccolta dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0e756-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="0e756-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="0e756-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="0e756-116">Specifica il nome della raccolta dell'area di lavoro per cui il cmdlet ottiene le aree di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0e756-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="0e756-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e756-117">CommonParameters</span></span>
<span data-ttu-id="0e756-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e756-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e756-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e756-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e756-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="0e756-120">INPUTS</span></span>

### <span data-ttu-id="0e756-121">System.String</span><span class="sxs-lookup"><span data-stu-id="0e756-121">System.String</span></span>

## <span data-ttu-id="0e756-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e756-122">OUTPUTS</span></span>

### <span data-ttu-id="0e756-123">Microsoft.Azure.Commands.Management.PowerBIE systemdded.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0e756-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="0e756-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="0e756-124">NOTES</span></span>

## <span data-ttu-id="0e756-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e756-125">RELATED LINKS</span></span>

[<span data-ttu-id="0e756-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0e756-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


