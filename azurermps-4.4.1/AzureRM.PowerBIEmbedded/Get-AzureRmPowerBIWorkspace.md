---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
ms.openlocfilehash: c7beab54a416809a3f5edd033d4c7946a16b807b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521179"
---
# <span data-ttu-id="01d8d-101">Get-AzureRmPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="01d8d-101">Get-AzureRmPowerBIWorkspace</span></span>

## <span data-ttu-id="01d8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="01d8d-103">Ottiene le aree di lavoro in una raccolta di un'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="01d8d-103">Gets the workspaces in a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01d8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01d8d-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01d8d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01d8d-105">DESCRIPTION</span></span>
<span data-ttu-id="01d8d-106">Il cmdlet **Get-AzureRmPowerBIWorkspace** ottiene le aree di lavoro in una raccolta di un'area di lavoro di Power bi.</span><span class="sxs-lookup"><span data-stu-id="01d8d-106">The **Get-AzureRmPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="01d8d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01d8d-107">EXAMPLES</span></span>

### <span data-ttu-id="01d8d-108">Esempio 1: recuperare le aree di lavoro di una raccolta di area di lavoro</span><span class="sxs-lookup"><span data-stu-id="01d8d-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="01d8d-109">Questo comando consente di ottenere le aree di lavoro che appartengono alla raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="01d8d-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="01d8d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01d8d-110">PARAMETERS</span></span>

### <span data-ttu-id="01d8d-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d8d-111">-ResourceGroupName</span></span>
<span data-ttu-id="01d8d-112">Specifica il nome del gruppo di risorse a cui appartiene la raccolta dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="01d8d-112">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="01d8d-113">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="01d8d-113">-WorkspaceCollectionName</span></span>
<span data-ttu-id="01d8d-114">Specifica il nome della raccolta dell'area di lavoro per cui questo cmdlet ottiene le aree di lavoro.</span><span class="sxs-lookup"><span data-stu-id="01d8d-114">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="01d8d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d8d-115">-DefaultProfile</span></span>
<span data-ttu-id="01d8d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01d8d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01d8d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d8d-117">CommonParameters</span></span>
<span data-ttu-id="01d8d-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01d8d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d8d-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01d8d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d8d-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01d8d-120">INPUTS</span></span>

## <span data-ttu-id="01d8d-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01d8d-121">OUTPUTS</span></span>

### <span data-ttu-id="01d8d-122">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="01d8d-122">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="01d8d-123">Note</span><span class="sxs-lookup"><span data-stu-id="01d8d-123">NOTES</span></span>

## <span data-ttu-id="01d8d-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01d8d-124">RELATED LINKS</span></span>

[<span data-ttu-id="01d8d-125">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="01d8d-125">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)


