---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmssinstance
schema: 2.0.0
ms.openlocfilehash: 07b068587848bc8af92fc49b039155c0a2c4fdd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866703"
---
# <span data-ttu-id="28750-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="28750-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="28750-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28750-102">SYNOPSIS</span></span>
<span data-ttu-id="28750-103">Avvia un aggiornamento manuale dell'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="28750-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28750-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28750-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28750-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28750-105">DESCRIPTION</span></span>
<span data-ttu-id="28750-106">Il cmdlet Update-AzureRmVmssInstance avvia un aggiornamento manuale dell'istanza di VMSS (Virtual Machine scale set) specificata.</span><span class="sxs-lookup"><span data-stu-id="28750-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="28750-107">Viene usato quando il criterio di aggiornamento del set di scale VMSS è impostato su Manual.</span><span class="sxs-lookup"><span data-stu-id="28750-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="28750-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28750-108">EXAMPLES</span></span>

### <span data-ttu-id="28750-109">Esempio 1: avviare un aggiornamento dell'istanza di VMSS</span><span class="sxs-lookup"><span data-stu-id="28750-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="28750-110">Questo comando avvia un aggiornamento della VMSS denominata VMScaleSet001 che contiene l'ID istanza di 0.</span><span class="sxs-lookup"><span data-stu-id="28750-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="28750-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28750-111">PARAMETERS</span></span>

### <span data-ttu-id="28750-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28750-112">-AsJob</span></span>
<span data-ttu-id="28750-113">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="28750-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="28750-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28750-114">-DefaultProfile</span></span>
<span data-ttu-id="28750-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28750-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28750-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="28750-116">-InstanceId</span></span>
<span data-ttu-id="28750-117">Specifica, come matrice di stringhe, l'ID o gli ID dell'istanza da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="28750-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28750-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28750-118">-ResourceGroupName</span></span>
<span data-ttu-id="28750-119">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="28750-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="28750-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="28750-120">-VMScaleSetName</span></span>
<span data-ttu-id="28750-121">Specifica il nome dell'istanza di VMSS che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="28750-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28750-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="28750-122">-Confirm</span></span>
<span data-ttu-id="28750-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28750-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28750-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28750-124">-WhatIf</span></span>
<span data-ttu-id="28750-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28750-125">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="28750-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28750-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28750-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28750-127">CommonParameters</span></span>
<span data-ttu-id="28750-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28750-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28750-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28750-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28750-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28750-130">INPUTS</span></span>

### <span data-ttu-id="28750-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="28750-131">None</span></span>
<span data-ttu-id="28750-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="28750-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="28750-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28750-133">OUTPUTS</span></span>

###  
<span data-ttu-id="28750-134">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="28750-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="28750-135">Note</span><span class="sxs-lookup"><span data-stu-id="28750-135">NOTES</span></span>

## <span data-ttu-id="28750-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28750-136">RELATED LINKS</span></span>

[<span data-ttu-id="28750-137">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="28750-137">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


