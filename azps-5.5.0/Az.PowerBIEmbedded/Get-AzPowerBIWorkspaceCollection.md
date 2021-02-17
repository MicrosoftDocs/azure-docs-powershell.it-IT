---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: d3be067690b755014fe02840d355fc36e0d6aa20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183966"
---
# <span data-ttu-id="6836f-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="6836f-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="6836f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6836f-102">SYNOPSIS</span></span>
<span data-ttu-id="6836f-103">Recupera le raccolte dell'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="6836f-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="6836f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6836f-104">SYNTAX</span></span>

### <span data-ttu-id="6836f-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="6836f-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6836f-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6836f-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6836f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6836f-107">DESCRIPTION</span></span>
<span data-ttu-id="6836f-108">Il cmdlet **Get-AzPowerBIWorkspaceCollection** ottiene le raccolte dell'area di lavoro di Power BI nell'abbonamento e nel gruppo di risorse di Azure oppure in base al nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="6836f-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="6836f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6836f-109">EXAMPLES</span></span>

### <span data-ttu-id="6836f-110">Esempio 1: Recuperare tutte le raccolte dell'area di lavoro in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6836f-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="6836f-111">Questo comando recupera le raccolte dell'area di lavoro che appartengono al gruppo di risorse denominato ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="6836f-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="6836f-112">Esempio 2: Ottenere una raccolta dell'area di lavoro usando il relativo nome</span><span class="sxs-lookup"><span data-stu-id="6836f-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="6836f-113">Questo comando recupera la raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="6836f-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="6836f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6836f-114">PARAMETERS</span></span>

### <span data-ttu-id="6836f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6836f-115">-DefaultProfile</span></span>
<span data-ttu-id="6836f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="6836f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6836f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6836f-117">-ResourceGroupName</span></span>
<span data-ttu-id="6836f-118">Specifica il nome del gruppo di risorse da cui il cmdlet ottiene le raccolte dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6836f-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

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

### <span data-ttu-id="6836f-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="6836f-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="6836f-120">Specifica il nome della raccolta dell'area di lavoro di Power BI recuperata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6836f-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6836f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6836f-121">CommonParameters</span></span>
<span data-ttu-id="6836f-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6836f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6836f-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6836f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6836f-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="6836f-124">INPUTS</span></span>

### <span data-ttu-id="6836f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="6836f-125">System.String</span></span>

## <span data-ttu-id="6836f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6836f-126">OUTPUTS</span></span>

### <span data-ttu-id="6836f-127">Microsoft.Azure.Commands.Management.PowerBIE systemdded.Models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="6836f-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="6836f-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="6836f-128">NOTES</span></span>

## <span data-ttu-id="6836f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6836f-129">RELATED LINKS</span></span>

[<span data-ttu-id="6836f-130">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="6836f-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="6836f-131">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="6836f-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


