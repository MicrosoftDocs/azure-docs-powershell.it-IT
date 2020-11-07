---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 8e029309099b3f28c1a9f0108bf4e6f4a78cb45d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865522"
---
# <span data-ttu-id="5affe-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5affe-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="5affe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5affe-102">SYNOPSIS</span></span>
<span data-ttu-id="5affe-103">Rimuove un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="5affe-103">Removes a container service.</span></span>

## <span data-ttu-id="5affe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5affe-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5affe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5affe-105">DESCRIPTION</span></span>
<span data-ttu-id="5affe-106">Il cmdlet **Remove-AzContainerService** rimuove un servizio contenitore dall'account Azure.</span><span class="sxs-lookup"><span data-stu-id="5affe-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="5affe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5affe-107">EXAMPLES</span></span>

### <span data-ttu-id="5affe-108">Esempio 1: rimuovere un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="5affe-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="5affe-109">Questo comando rimuove il servizio contenitore denominato CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="5affe-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="5affe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5affe-110">PARAMETERS</span></span>

### <span data-ttu-id="5affe-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5affe-111">-AsJob</span></span>
<span data-ttu-id="5affe-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="5affe-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5affe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5affe-113">-DefaultProfile</span></span>
<span data-ttu-id="5affe-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5affe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5affe-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5affe-115">-Force</span></span>
<span data-ttu-id="5affe-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5affe-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5affe-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5affe-117">-Name</span></span>
<span data-ttu-id="5affe-118">Specifica il nome del servizio contenitore rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5affe-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5affe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5affe-119">-ResourceGroupName</span></span>
<span data-ttu-id="5affe-120">Specifica il gruppo di risorse del servizio contenitore rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5affe-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5affe-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5affe-121">-Confirm</span></span>
<span data-ttu-id="5affe-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5affe-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5affe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5affe-123">-WhatIf</span></span>
<span data-ttu-id="5affe-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5affe-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5affe-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5affe-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5affe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5affe-126">CommonParameters</span></span>
<span data-ttu-id="5affe-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5affe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5affe-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5affe-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5affe-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5affe-129">INPUTS</span></span>

### <span data-ttu-id="5affe-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5affe-130">System.String</span></span>

## <span data-ttu-id="5affe-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5affe-131">OUTPUTS</span></span>

### <span data-ttu-id="5affe-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="5affe-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="5affe-133">Note</span><span class="sxs-lookup"><span data-stu-id="5affe-133">NOTES</span></span>

## <span data-ttu-id="5affe-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5affe-134">RELATED LINKS</span></span>

[<span data-ttu-id="5affe-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5affe-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="5affe-136">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5affe-136">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="5affe-137">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5affe-137">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


