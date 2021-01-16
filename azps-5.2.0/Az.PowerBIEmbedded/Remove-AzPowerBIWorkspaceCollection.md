---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: c8e6f54b5bd4deeb4ef24559298306880740c6d3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349231"
---
# <span data-ttu-id="5f3ea-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="5f3ea-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="5f3ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="5f3ea-103">Rimuove una raccolta di un'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="5f3ea-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="5f3ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f3ea-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f3ea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f3ea-105">DESCRIPTION</span></span>
<span data-ttu-id="5f3ea-106">Il cmdlet **Remove-AzPowerBIWorkspaceCollection** rimuove una raccolta di un'area di lavoro di Power BI dal gruppo di risorse e dell'abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="5f3ea-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="5f3ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f3ea-107">EXAMPLES</span></span>

### <span data-ttu-id="5f3ea-108">Esempio 1: rimuovere una raccolta di un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="5f3ea-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="5f3ea-109">Questo comando rimuove la raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="5f3ea-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="5f3ea-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f3ea-110">PARAMETERS</span></span>

### <span data-ttu-id="5f3ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f3ea-111">-DefaultProfile</span></span>
<span data-ttu-id="5f3ea-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5f3ea-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f3ea-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f3ea-113">-ResourceGroupName</span></span>
<span data-ttu-id="5f3ea-114">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove una raccolta di area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5f3ea-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="5f3ea-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="5f3ea-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="5f3ea-116">Specifica il nome della raccolta dell'area di lavoro di Power BI rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f3ea-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5f3ea-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5f3ea-117">-Confirm</span></span>
<span data-ttu-id="5f3ea-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f3ea-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f3ea-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f3ea-119">-WhatIf</span></span>
<span data-ttu-id="5f3ea-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f3ea-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f3ea-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f3ea-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f3ea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f3ea-122">CommonParameters</span></span>
<span data-ttu-id="5f3ea-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f3ea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f3ea-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f3ea-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f3ea-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f3ea-125">INPUTS</span></span>

### <span data-ttu-id="5f3ea-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5f3ea-126">System.String</span></span>

## <span data-ttu-id="5f3ea-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f3ea-127">OUTPUTS</span></span>

### <span data-ttu-id="5f3ea-128">System. void</span><span class="sxs-lookup"><span data-stu-id="5f3ea-128">System.Void</span></span>

## <span data-ttu-id="5f3ea-129">Note</span><span class="sxs-lookup"><span data-stu-id="5f3ea-129">NOTES</span></span>

## <span data-ttu-id="5f3ea-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f3ea-130">RELATED LINKS</span></span>

[<span data-ttu-id="5f3ea-131">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="5f3ea-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="5f3ea-132">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="5f3ea-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)


