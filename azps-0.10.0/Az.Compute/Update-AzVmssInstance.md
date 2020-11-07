---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: d8fb3b740a85b4cb258fcfa08bf9f4e06032fcb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861573"
---
# <span data-ttu-id="aaaf3-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="aaaf3-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="aaaf3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aaaf3-102">SYNOPSIS</span></span>
<span data-ttu-id="aaaf3-103">Avvia un aggiornamento manuale dell'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="aaaf3-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="aaaf3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aaaf3-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaaf3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aaaf3-105">DESCRIPTION</span></span>
<span data-ttu-id="aaaf3-106">Il cmdlet Update-AzVmssInstance avvia un aggiornamento manuale dell'istanza di VMSS (Virtual Machine scale set) specificata.</span><span class="sxs-lookup"><span data-stu-id="aaaf3-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="aaaf3-107">Viene usato quando il criterio di aggiornamento del set di scale VMSS è impostato su Manual.</span><span class="sxs-lookup"><span data-stu-id="aaaf3-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="aaaf3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aaaf3-108">EXAMPLES</span></span>

### <span data-ttu-id="aaaf3-109">Esempio 1: avviare un aggiornamento dell'istanza di VMSS</span><span class="sxs-lookup"><span data-stu-id="aaaf3-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="aaaf3-110">Questo comando avvia un aggiornamento della VMSS denominata VMScaleSet001 che contiene l'ID istanza di 0.</span><span class="sxs-lookup"><span data-stu-id="aaaf3-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="aaaf3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aaaf3-111">PARAMETERS</span></span>

### <span data-ttu-id="aaaf3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aaaf3-112">-AsJob</span></span>
<span data-ttu-id="aaaf3-113">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="aaaf3-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="aaaf3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaaf3-114">-DefaultProfile</span></span>
<span data-ttu-id="aaaf3-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aaaf3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaaf3-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="aaaf3-116">-InstanceId</span></span>
<span data-ttu-id="aaaf3-117">Specifica, come matrice di stringhe, l'ID o gli ID dell'istanza da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="aaaf3-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

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

### <span data-ttu-id="aaaf3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaaf3-118">-ResourceGroupName</span></span>
<span data-ttu-id="aaaf3-119">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="aaaf3-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="aaaf3-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="aaaf3-120">-VMScaleSetName</span></span>
<span data-ttu-id="aaaf3-121">Specifica il nome dell'istanza di VMSS che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="aaaf3-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="aaaf3-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aaaf3-122">-Confirm</span></span>
<span data-ttu-id="aaaf3-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaaf3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaaf3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaaf3-124">-WhatIf</span></span>
<span data-ttu-id="aaaf3-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aaaf3-125">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="aaaf3-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aaaf3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaaf3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaaf3-127">CommonParameters</span></span>
<span data-ttu-id="aaaf3-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaaf3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaaf3-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaaf3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaaf3-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aaaf3-130">INPUTS</span></span>

### <span data-ttu-id="aaaf3-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="aaaf3-131">None</span></span>
<span data-ttu-id="aaaf3-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="aaaf3-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aaaf3-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aaaf3-133">OUTPUTS</span></span>

###  
<span data-ttu-id="aaaf3-134">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="aaaf3-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="aaaf3-135">Note</span><span class="sxs-lookup"><span data-stu-id="aaaf3-135">NOTES</span></span>

## <span data-ttu-id="aaaf3-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aaaf3-136">RELATED LINKS</span></span>

[<span data-ttu-id="aaaf3-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aaaf3-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


