---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 5a2a8157e69c1b50cc066bb24e8261c1748a6323
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863589"
---
# <span data-ttu-id="48043-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="48043-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="48043-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48043-102">SYNOPSIS</span></span>
<span data-ttu-id="48043-103">Rimuove un set di disponibilità da Azure.</span><span class="sxs-lookup"><span data-stu-id="48043-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="48043-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48043-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48043-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48043-105">DESCRIPTION</span></span>
<span data-ttu-id="48043-106">Il cmdlet **Remove-AzAvailabilitySet** rimuove un set di disponibilità da Azure.</span><span class="sxs-lookup"><span data-stu-id="48043-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="48043-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48043-107">EXAMPLES</span></span>

### <span data-ttu-id="48043-108">Esempio 1: rimuovere un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="48043-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="48043-109">Questo comando rimuove un set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="48043-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="48043-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48043-110">PARAMETERS</span></span>

### <span data-ttu-id="48043-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48043-111">-AsJob</span></span>
<span data-ttu-id="48043-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="48043-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="48043-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48043-113">-DefaultProfile</span></span>
<span data-ttu-id="48043-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48043-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48043-115">-Force</span><span class="sxs-lookup"><span data-stu-id="48043-115">-Force</span></span>
<span data-ttu-id="48043-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="48043-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="48043-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="48043-117">-Name</span></span>
<span data-ttu-id="48043-118">Nome del set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="48043-118">The availability set name.</span></span>

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

### <span data-ttu-id="48043-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48043-119">-ResourceGroupName</span></span>
<span data-ttu-id="48043-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="48043-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="48043-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="48043-121">-Confirm</span></span>
<span data-ttu-id="48043-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48043-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48043-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48043-123">-WhatIf</span></span>
<span data-ttu-id="48043-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48043-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="48043-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48043-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48043-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48043-126">CommonParameters</span></span>
<span data-ttu-id="48043-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48043-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48043-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48043-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48043-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48043-129">INPUTS</span></span>

### <span data-ttu-id="48043-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="48043-130">None</span></span>
<span data-ttu-id="48043-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="48043-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="48043-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48043-132">OUTPUTS</span></span>

### <span data-ttu-id="48043-133">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="48043-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="48043-134">Note</span><span class="sxs-lookup"><span data-stu-id="48043-134">NOTES</span></span>

## <span data-ttu-id="48043-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48043-135">RELATED LINKS</span></span>

[<span data-ttu-id="48043-136">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="48043-136">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="48043-137">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="48043-137">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


