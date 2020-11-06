---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 7d7fefad86534cd2614312b21bd3ac392050e1b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513548"
---
# <span data-ttu-id="d31a2-101">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="d31a2-101">Get-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="d31a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d31a2-102">SYNOPSIS</span></span>
<span data-ttu-id="d31a2-103">Ottiene le raccolte dell'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="d31a2-103">Gets Power BI workspace collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d31a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d31a2-104">SYNTAX</span></span>

### <span data-ttu-id="d31a2-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="d31a2-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d31a2-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d31a2-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d31a2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d31a2-107">DESCRIPTION</span></span>
<span data-ttu-id="d31a2-108">Il cmdlet **Get-AzureRmPowerBIWorkspaceCollection** ottiene le raccolte dell'area di lavoro di Power bi nel gruppo di sottoscrizione e delle risorse di Azure oppure in base al nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d31a2-108">The **Get-AzureRmPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="d31a2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d31a2-109">EXAMPLES</span></span>

### <span data-ttu-id="d31a2-110">Esempio 1: ottenere tutte le raccolte dell'area di lavoro in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d31a2-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="d31a2-111">Questo comando consente di ottenere le raccolte dell'area di lavoro che appartengono al gruppo di risorse denominato ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="d31a2-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="d31a2-112">Esempio 2: ottenere una raccolta dell'area di lavoro usando il relativo nome</span><span class="sxs-lookup"><span data-stu-id="d31a2-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="d31a2-113">Questo comando ottiene la raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="d31a2-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="d31a2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d31a2-114">PARAMETERS</span></span>

### <span data-ttu-id="d31a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d31a2-115">-DefaultProfile</span></span>
<span data-ttu-id="d31a2-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d31a2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d31a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d31a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="d31a2-118">Specifica il nome del gruppo di risorse da cui questo cmdlet ottiene le raccolte dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d31a2-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d31a2-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="d31a2-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="d31a2-120">Specifica il nome della raccolta dell'area di lavoro di Power BI ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d31a2-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d31a2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d31a2-121">CommonParameters</span></span>
<span data-ttu-id="d31a2-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d31a2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d31a2-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d31a2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d31a2-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d31a2-124">INPUTS</span></span>

### <span data-ttu-id="d31a2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d31a2-125">System.String</span></span>

## <span data-ttu-id="d31a2-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d31a2-126">OUTPUTS</span></span>

### <span data-ttu-id="d31a2-127">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="d31a2-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="d31a2-128">Note</span><span class="sxs-lookup"><span data-stu-id="d31a2-128">NOTES</span></span>

## <span data-ttu-id="d31a2-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d31a2-129">RELATED LINKS</span></span>

[<span data-ttu-id="d31a2-130">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="d31a2-130">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="d31a2-131">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="d31a2-131">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


