---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 27d1e45a9e2c85fb3d2f7470db97ce2426f62a19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866730"
---
# <span data-ttu-id="7e76b-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="7e76b-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="7e76b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e76b-102">SYNOPSIS</span></span>
<span data-ttu-id="7e76b-103">Rimuove un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="7e76b-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e76b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e76b-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e76b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e76b-105">DESCRIPTION</span></span>
<span data-ttu-id="7e76b-106">Il cmdlet **Remove-AzureRmContainerService** rimuove un servizio contenitore dall'account Azure.</span><span class="sxs-lookup"><span data-stu-id="7e76b-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="7e76b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e76b-107">EXAMPLES</span></span>

### <span data-ttu-id="7e76b-108">Esempio 1: rimuovere un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="7e76b-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="7e76b-109">Questo comando rimuove il servizio contenitore denominato CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="7e76b-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="7e76b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e76b-110">PARAMETERS</span></span>

### <span data-ttu-id="7e76b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e76b-111">-AsJob</span></span>
<span data-ttu-id="7e76b-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="7e76b-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e76b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e76b-113">-DefaultProfile</span></span>
<span data-ttu-id="7e76b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e76b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e76b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7e76b-115">-Force</span></span>
<span data-ttu-id="7e76b-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7e76b-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e76b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e76b-117">-Name</span></span>
<span data-ttu-id="7e76b-118">Specifica il nome del servizio contenitore rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e76b-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e76b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e76b-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e76b-120">Specifica il gruppo di risorse del servizio contenitore rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e76b-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e76b-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7e76b-121">-Confirm</span></span>
<span data-ttu-id="7e76b-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e76b-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="7e76b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e76b-123">-WhatIf</span></span>
<span data-ttu-id="7e76b-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e76b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e76b-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e76b-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="7e76b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e76b-126">CommonParameters</span></span>
<span data-ttu-id="7e76b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e76b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e76b-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e76b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e76b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e76b-129">INPUTS</span></span>

### <span data-ttu-id="7e76b-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7e76b-130">None</span></span>
<span data-ttu-id="7e76b-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7e76b-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e76b-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e76b-132">OUTPUTS</span></span>

### <span data-ttu-id="7e76b-133">System. void</span><span class="sxs-lookup"><span data-stu-id="7e76b-133">System.Void</span></span>

## <span data-ttu-id="7e76b-134">Note</span><span class="sxs-lookup"><span data-stu-id="7e76b-134">NOTES</span></span>

## <span data-ttu-id="7e76b-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e76b-135">RELATED LINKS</span></span>

[<span data-ttu-id="7e76b-136">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="7e76b-136">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="7e76b-137">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="7e76b-137">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="7e76b-138">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="7e76b-138">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


