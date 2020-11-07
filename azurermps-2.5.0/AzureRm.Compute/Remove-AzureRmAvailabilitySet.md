---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: cc8292940a252844c0aeabe820eec2e62055c954
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866731"
---
# <span data-ttu-id="e6e47-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e6e47-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="e6e47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6e47-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e47-103">Rimuove un set di disponibilità da Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e47-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6e47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6e47-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6e47-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6e47-105">DESCRIPTION</span></span>
<span data-ttu-id="e6e47-106">Il cmdlet **Remove-AzureRmAvailabilitySet** rimuove un set di disponibilità da Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e47-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="e6e47-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6e47-107">EXAMPLES</span></span>

### <span data-ttu-id="e6e47-108">Esempio 1: rimuovere un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="e6e47-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="e6e47-109">Questo comando rimuove un set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e6e47-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="e6e47-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6e47-110">PARAMETERS</span></span>

### <span data-ttu-id="e6e47-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6e47-111">-AsJob</span></span>
<span data-ttu-id="e6e47-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="e6e47-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e6e47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e47-113">-DefaultProfile</span></span>
<span data-ttu-id="e6e47-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e47-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6e47-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e6e47-115">-Force</span></span>
<span data-ttu-id="e6e47-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e6e47-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e47-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6e47-117">-Name</span></span>
<span data-ttu-id="e6e47-118">Nome del set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="e6e47-118">The availability set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e47-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6e47-119">-ResourceGroupName</span></span>
<span data-ttu-id="e6e47-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e6e47-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e6e47-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e6e47-121">-Confirm</span></span>
<span data-ttu-id="e6e47-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6e47-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6e47-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6e47-123">-WhatIf</span></span>
<span data-ttu-id="e6e47-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6e47-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e6e47-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6e47-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6e47-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e47-126">CommonParameters</span></span>
<span data-ttu-id="e6e47-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6e47-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e47-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6e47-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e47-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6e47-129">INPUTS</span></span>

### <span data-ttu-id="e6e47-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e6e47-130">None</span></span>
<span data-ttu-id="e6e47-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e6e47-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e6e47-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6e47-132">OUTPUTS</span></span>

### <span data-ttu-id="e6e47-133">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e6e47-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e6e47-134">Note</span><span class="sxs-lookup"><span data-stu-id="e6e47-134">NOTES</span></span>

## <span data-ttu-id="e6e47-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6e47-135">RELATED LINKS</span></span>

[<span data-ttu-id="e6e47-136">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e6e47-136">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="e6e47-137">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e6e47-137">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


