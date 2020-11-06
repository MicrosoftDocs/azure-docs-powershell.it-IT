---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: 19c94fae0192766b87f430e6137fe8d3652325c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511835"
---
# <span data-ttu-id="46349-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="46349-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="46349-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="46349-102">SYNOPSIS</span></span>
<span data-ttu-id="46349-103">Rimuove un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="46349-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46349-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46349-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46349-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46349-105">DESCRIPTION</span></span>
<span data-ttu-id="46349-106">Il cmdlet **Remove-AzureRmContainerService** rimuove un servizio contenitore dall'account Azure.</span><span class="sxs-lookup"><span data-stu-id="46349-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="46349-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46349-107">EXAMPLES</span></span>

### <span data-ttu-id="46349-108">Esempio 1: rimuovere un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="46349-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="46349-109">Questo comando rimuove il servizio contenitore denominato CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="46349-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="46349-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="46349-110">PARAMETERS</span></span>

### <span data-ttu-id="46349-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46349-111">-AsJob</span></span>
<span data-ttu-id="46349-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="46349-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="46349-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46349-113">-DefaultProfile</span></span>
<span data-ttu-id="46349-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46349-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46349-115">-Force</span><span class="sxs-lookup"><span data-stu-id="46349-115">-Force</span></span>
<span data-ttu-id="46349-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="46349-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="46349-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="46349-117">-Name</span></span>
<span data-ttu-id="46349-118">Specifica il nome del servizio contenitore rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46349-118">Specifies the name of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="46349-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46349-119">-ResourceGroupName</span></span>
<span data-ttu-id="46349-120">Specifica il gruppo di risorse del servizio contenitore rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46349-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="46349-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="46349-121">-Confirm</span></span>
<span data-ttu-id="46349-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46349-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46349-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46349-123">-WhatIf</span></span>
<span data-ttu-id="46349-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46349-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46349-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46349-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46349-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46349-126">CommonParameters</span></span>
<span data-ttu-id="46349-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46349-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46349-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46349-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46349-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="46349-129">INPUTS</span></span>

### <span data-ttu-id="46349-130">System. String</span><span class="sxs-lookup"><span data-stu-id="46349-130">System.String</span></span>

## <span data-ttu-id="46349-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46349-131">OUTPUTS</span></span>

### <span data-ttu-id="46349-132">System. void</span><span class="sxs-lookup"><span data-stu-id="46349-132">System.Void</span></span>

## <span data-ttu-id="46349-133">Note</span><span class="sxs-lookup"><span data-stu-id="46349-133">NOTES</span></span>

## <span data-ttu-id="46349-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46349-134">RELATED LINKS</span></span>

[<span data-ttu-id="46349-135">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="46349-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="46349-136">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="46349-136">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="46349-137">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="46349-137">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


