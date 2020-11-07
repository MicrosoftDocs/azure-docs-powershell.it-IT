---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 7f3a48db5d8f1e6c7b4b0e73b705fc375a0b514f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687481"
---
# <span data-ttu-id="e05d0-101">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="e05d0-101">Remove-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="e05d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e05d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e05d0-103">Rimuove una raccolta di un'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="e05d0-103">Removes a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e05d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e05d0-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e05d0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e05d0-105">DESCRIPTION</span></span>
<span data-ttu-id="e05d0-106">Il cmdlet **Remove-AzureRmPowerBIWorkspaceCollection** rimuove una raccolta di un'area di lavoro di Power BI dal gruppo di risorse e dell'abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="e05d0-106">The **Remove-AzureRmPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="e05d0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e05d0-107">EXAMPLES</span></span>

### <span data-ttu-id="e05d0-108">Esempio 1: rimuovere una raccolta di un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="e05d0-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="e05d0-109">Questo comando rimuove la raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="e05d0-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="e05d0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e05d0-110">PARAMETERS</span></span>

### <span data-ttu-id="e05d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05d0-111">-DefaultProfile</span></span>
<span data-ttu-id="e05d0-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e05d0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05d0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e05d0-113">-ResourceGroupName</span></span>
<span data-ttu-id="e05d0-114">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove una raccolta di area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e05d0-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05d0-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="e05d0-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="e05d0-116">Specifica il nome della raccolta dell'area di lavoro di Power BI rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e05d0-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05d0-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e05d0-117">-Confirm</span></span>
<span data-ttu-id="e05d0-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e05d0-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05d0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e05d0-119">-WhatIf</span></span>
<span data-ttu-id="e05d0-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e05d0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e05d0-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e05d0-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05d0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05d0-122">CommonParameters</span></span>
<span data-ttu-id="e05d0-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e05d0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05d0-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e05d0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05d0-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e05d0-125">INPUTS</span></span>

### <span data-ttu-id="e05d0-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e05d0-126">None</span></span>
<span data-ttu-id="e05d0-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e05d0-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e05d0-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e05d0-128">OUTPUTS</span></span>

## <span data-ttu-id="e05d0-129">Note</span><span class="sxs-lookup"><span data-stu-id="e05d0-129">NOTES</span></span>

## <span data-ttu-id="e05d0-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e05d0-130">RELATED LINKS</span></span>

[<span data-ttu-id="e05d0-131">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="e05d0-131">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="e05d0-132">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="e05d0-132">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)


