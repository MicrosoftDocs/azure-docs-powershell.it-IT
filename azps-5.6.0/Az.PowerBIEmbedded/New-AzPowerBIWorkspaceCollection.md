---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 69f90f84d7e142ea3471c7e6871baac145f1b9c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974526"
---
# <span data-ttu-id="09f3e-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="09f3e-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="09f3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="09f3e-103">Crea una raccolta di aree di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="09f3e-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="09f3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09f3e-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09f3e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="09f3e-105">DESCRIPTION</span></span>
<span data-ttu-id="09f3e-106">Il cmdlet **New-AzPowerBIWorkspaceCollection** crea una raccolta di aree di lavoro di Power BI per la sottoscrizione di Azure nel gruppo di risorse e nella posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="09f3e-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="09f3e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09f3e-107">EXAMPLES</span></span>

### <span data-ttu-id="09f3e-108">Esempio 1: Creare una raccolta dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="09f3e-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="09f3e-109">Questo comando crea una raccolta di aree di lavoro denominata WCN11 nel gruppo di risorse specificato nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="09f3e-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="09f3e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09f3e-110">PARAMETERS</span></span>

### <span data-ttu-id="09f3e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f3e-111">-DefaultProfile</span></span>
<span data-ttu-id="09f3e-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="09f3e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09f3e-113">-Location</span><span class="sxs-lookup"><span data-stu-id="09f3e-113">-Location</span></span>
<span data-ttu-id="09f3e-114">Specifica la posizione di Azure in cui questo cmdlet crea una raccolta dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="09f3e-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09f3e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09f3e-115">-ResourceGroupName</span></span>
<span data-ttu-id="09f3e-116">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una raccolta dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="09f3e-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="09f3e-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="09f3e-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="09f3e-118">Specifica un nome per la raccolta dell'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="09f3e-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="09f3e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09f3e-119">-Confirm</span></span>
<span data-ttu-id="09f3e-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09f3e-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f3e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09f3e-121">-WhatIf</span></span>
<span data-ttu-id="09f3e-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09f3e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09f3e-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09f3e-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f3e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f3e-124">CommonParameters</span></span>
<span data-ttu-id="09f3e-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f3e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f3e-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09f3e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f3e-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="09f3e-127">INPUTS</span></span>

### <span data-ttu-id="09f3e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="09f3e-128">System.String</span></span>

## <span data-ttu-id="09f3e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09f3e-129">OUTPUTS</span></span>

### <span data-ttu-id="09f3e-130">Microsoft.Azure.Commands.Management.PowerBIE systemdded.Models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="09f3e-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="09f3e-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="09f3e-131">NOTES</span></span>

## <span data-ttu-id="09f3e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09f3e-132">RELATED LINKS</span></span>

[<span data-ttu-id="09f3e-133">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="09f3e-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="09f3e-134">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="09f3e-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


