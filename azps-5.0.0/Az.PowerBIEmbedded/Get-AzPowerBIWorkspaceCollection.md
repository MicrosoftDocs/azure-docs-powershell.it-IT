---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: d3be067690b755014fe02840d355fc36e0d6aa20
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199484"
---
# <span data-ttu-id="85889-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="85889-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="85889-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85889-102">SYNOPSIS</span></span>
<span data-ttu-id="85889-103">Ottiene le raccolte dell'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="85889-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="85889-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85889-104">SYNTAX</span></span>

### <span data-ttu-id="85889-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="85889-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85889-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="85889-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85889-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85889-107">DESCRIPTION</span></span>
<span data-ttu-id="85889-108">Il cmdlet **Get-AzPowerBIWorkspaceCollection** ottiene le raccolte dell'area di lavoro di Power bi nel gruppo di sottoscrizione e delle risorse di Azure oppure in base al nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="85889-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="85889-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85889-109">EXAMPLES</span></span>

### <span data-ttu-id="85889-110">Esempio 1: ottenere tutte le raccolte dell'area di lavoro in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="85889-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="85889-111">Questo comando consente di ottenere le raccolte dell'area di lavoro che appartengono al gruppo di risorse denominato ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="85889-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="85889-112">Esempio 2: ottenere una raccolta dell'area di lavoro usando il relativo nome</span><span class="sxs-lookup"><span data-stu-id="85889-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="85889-113">Questo comando ottiene la raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="85889-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="85889-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85889-114">PARAMETERS</span></span>

### <span data-ttu-id="85889-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85889-115">-DefaultProfile</span></span>
<span data-ttu-id="85889-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="85889-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85889-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85889-117">-ResourceGroupName</span></span>
<span data-ttu-id="85889-118">Specifica il nome del gruppo di risorse da cui questo cmdlet ottiene le raccolte dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="85889-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

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

### <span data-ttu-id="85889-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="85889-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="85889-120">Specifica il nome della raccolta dell'area di lavoro di Power BI ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85889-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

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

### <span data-ttu-id="85889-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85889-121">CommonParameters</span></span>
<span data-ttu-id="85889-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85889-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85889-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85889-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85889-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85889-124">INPUTS</span></span>

### <span data-ttu-id="85889-125">System. String</span><span class="sxs-lookup"><span data-stu-id="85889-125">System.String</span></span>

## <span data-ttu-id="85889-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85889-126">OUTPUTS</span></span>

### <span data-ttu-id="85889-127">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="85889-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="85889-128">Note</span><span class="sxs-lookup"><span data-stu-id="85889-128">NOTES</span></span>

## <span data-ttu-id="85889-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85889-129">RELATED LINKS</span></span>

[<span data-ttu-id="85889-130">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="85889-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="85889-131">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="85889-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


