---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
ms.openlocfilehash: 2217a6940e5f740c2499e95ff05f67c7144cbc3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685761"
---
# <span data-ttu-id="57d05-101">Get-AzureRmPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="57d05-101">Get-AzureRmPowerBIWorkspace</span></span>

## <span data-ttu-id="57d05-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57d05-102">SYNOPSIS</span></span>
<span data-ttu-id="57d05-103">Ottiene le aree di lavoro in una raccolta di un'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="57d05-103">Gets the workspaces in a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57d05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57d05-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57d05-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57d05-105">DESCRIPTION</span></span>
<span data-ttu-id="57d05-106">Il cmdlet **Get-AzureRmPowerBIWorkspace** ottiene le aree di lavoro in una raccolta di un'area di lavoro di Power bi.</span><span class="sxs-lookup"><span data-stu-id="57d05-106">The **Get-AzureRmPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="57d05-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57d05-107">EXAMPLES</span></span>

### <span data-ttu-id="57d05-108">Esempio 1: recuperare le aree di lavoro di una raccolta di area di lavoro</span><span class="sxs-lookup"><span data-stu-id="57d05-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="57d05-109">Questo comando consente di ottenere le aree di lavoro che appartengono alla raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="57d05-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="57d05-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57d05-110">PARAMETERS</span></span>

### <span data-ttu-id="57d05-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d05-111">-DefaultProfile</span></span>
<span data-ttu-id="57d05-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="57d05-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57d05-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57d05-113">-ResourceGroupName</span></span>
<span data-ttu-id="57d05-114">Specifica il nome del gruppo di risorse a cui appartiene la raccolta dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="57d05-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="57d05-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="57d05-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="57d05-116">Specifica il nome della raccolta dell'area di lavoro per cui questo cmdlet ottiene le aree di lavoro.</span><span class="sxs-lookup"><span data-stu-id="57d05-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="57d05-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d05-117">CommonParameters</span></span>
<span data-ttu-id="57d05-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57d05-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d05-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57d05-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d05-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57d05-120">INPUTS</span></span>

### <span data-ttu-id="57d05-121">System. String</span><span class="sxs-lookup"><span data-stu-id="57d05-121">System.String</span></span>

## <span data-ttu-id="57d05-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57d05-122">OUTPUTS</span></span>

### <span data-ttu-id="57d05-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="57d05-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="57d05-124">Note</span><span class="sxs-lookup"><span data-stu-id="57d05-124">NOTES</span></span>

## <span data-ttu-id="57d05-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57d05-125">RELATED LINKS</span></span>

[<span data-ttu-id="57d05-126">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="57d05-126">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)


