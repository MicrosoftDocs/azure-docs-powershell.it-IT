---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 1623b706a3878b517680782462e07ebacce2daf9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953438"
---
# <span data-ttu-id="0a9cc-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0a9cc-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="0a9cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a9cc-102">SYNOPSIS</span></span>
<span data-ttu-id="0a9cc-103">Rimuove una raccolta di aree di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="0a9cc-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="0a9cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a9cc-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a9cc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0a9cc-105">DESCRIPTION</span></span>
<span data-ttu-id="0a9cc-106">Il cmdlet **Remove-AzPowerBIWorkspaceCollection** rimuove una raccolta di aree di lavoro di Power BI dalla sottoscrizione e dal gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a9cc-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="0a9cc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a9cc-107">EXAMPLES</span></span>

### <span data-ttu-id="0a9cc-108">Esempio 1: Rimuovere una raccolta di aree di lavoro</span><span class="sxs-lookup"><span data-stu-id="0a9cc-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="0a9cc-109">Questo comando rimuove la raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="0a9cc-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="0a9cc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a9cc-110">PARAMETERS</span></span>

### <span data-ttu-id="0a9cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a9cc-111">-DefaultProfile</span></span>
<span data-ttu-id="0a9cc-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0a9cc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a9cc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a9cc-113">-ResourceGroupName</span></span>
<span data-ttu-id="0a9cc-114">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove una raccolta di aree di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0a9cc-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="0a9cc-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="0a9cc-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="0a9cc-116">Specifica il nome della raccolta dell'area di lavoro di Power BI rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a9cc-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0a9cc-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a9cc-117">-Confirm</span></span>
<span data-ttu-id="0a9cc-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a9cc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a9cc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a9cc-119">-WhatIf</span></span>
<span data-ttu-id="0a9cc-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a9cc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a9cc-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a9cc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a9cc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a9cc-122">CommonParameters</span></span>
<span data-ttu-id="0a9cc-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a9cc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a9cc-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a9cc-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a9cc-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="0a9cc-125">INPUTS</span></span>

### <span data-ttu-id="0a9cc-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0a9cc-126">System.String</span></span>

## <span data-ttu-id="0a9cc-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a9cc-127">OUTPUTS</span></span>

### <span data-ttu-id="0a9cc-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="0a9cc-128">System.Void</span></span>

## <span data-ttu-id="0a9cc-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="0a9cc-129">NOTES</span></span>

## <span data-ttu-id="0a9cc-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a9cc-130">RELATED LINKS</span></span>

[<span data-ttu-id="0a9cc-131">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0a9cc-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="0a9cc-132">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0a9cc-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)


