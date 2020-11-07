---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
ms.openlocfilehash: c5fcd5f4e331c55fb95a0d8657a59a944be585c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678756"
---
# <span data-ttu-id="51c48-101">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="51c48-101">Remove-AzAutoscaleSetting</span></span>

## <span data-ttu-id="51c48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51c48-102">SYNOPSIS</span></span>
<span data-ttu-id="51c48-103">Rimuove un'impostazione di scala.</span><span class="sxs-lookup"><span data-stu-id="51c48-103">Removes an Autoscale setting.</span></span>

## <span data-ttu-id="51c48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51c48-104">SYNTAX</span></span>

```
Remove-AzAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51c48-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51c48-105">DESCRIPTION</span></span>
<span data-ttu-id="51c48-106">Il cmdlet **Remove-AzAutoscaleSetting** rimuove un'impostazione di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="51c48-106">The **Remove-AzAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="51c48-107">Devi specificare il nome dell'impostazione e il nome del gruppo di risorse a cui è assegnato.</span><span class="sxs-lookup"><span data-stu-id="51c48-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="51c48-108">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="51c48-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="51c48-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51c48-109">EXAMPLES</span></span>

## <span data-ttu-id="51c48-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51c48-110">PARAMETERS</span></span>

### <span data-ttu-id="51c48-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51c48-111">-DefaultProfile</span></span>
<span data-ttu-id="51c48-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="51c48-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51c48-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="51c48-113">-Name</span></span>
<span data-ttu-id="51c48-114">Specifica il nome dell'impostazione di scalabilità verticale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="51c48-114">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c48-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51c48-115">-ResourceGroupName</span></span>
<span data-ttu-id="51c48-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="51c48-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c48-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="51c48-117">-Confirm</span></span>
<span data-ttu-id="51c48-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51c48-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51c48-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51c48-119">-WhatIf</span></span>
<span data-ttu-id="51c48-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51c48-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51c48-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51c48-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51c48-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51c48-122">CommonParameters</span></span>
<span data-ttu-id="51c48-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51c48-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51c48-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51c48-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51c48-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51c48-125">INPUTS</span></span>

### <span data-ttu-id="51c48-126">System. String</span><span class="sxs-lookup"><span data-stu-id="51c48-126">System.String</span></span>

## <span data-ttu-id="51c48-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51c48-127">OUTPUTS</span></span>

### <span data-ttu-id="51c48-128">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="51c48-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="51c48-129">Note</span><span class="sxs-lookup"><span data-stu-id="51c48-129">NOTES</span></span>

## <span data-ttu-id="51c48-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51c48-130">RELATED LINKS</span></span>

[<span data-ttu-id="51c48-131">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="51c48-131">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="51c48-132">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="51c48-132">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)


