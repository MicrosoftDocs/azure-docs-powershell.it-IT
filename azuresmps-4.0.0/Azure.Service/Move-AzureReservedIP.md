---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D1A4FA07-C25E-472B-9C64-695AD41274FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb8b6a502d6abe5520cadcf776ece1f077c7d91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029704"
---
# <span data-ttu-id="c8f1e-101">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="c8f1e-101">Move-AzureReservedIP</span></span>

## <span data-ttu-id="c8f1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f1e-103">Esegue la migrazione di un indirizzo IP riservato allo stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="c8f1e-103">Migrates a reserved IP address to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="c8f1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8f1e-104">SYNTAX</span></span>

### <span data-ttu-id="c8f1e-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8f1e-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8f1e-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8f1e-106">AbortMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8f1e-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8f1e-107">CommitMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8f1e-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8f1e-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8f1e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8f1e-109">DESCRIPTION</span></span>
<span data-ttu-id="c8f1e-110">Il cmdlet **Move-AzureReservedIP** esegue la migrazione di un indirizzo IP riservato a un gruppo di risorse nello stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="c8f1e-110">The **Move-AzureReservedIP** cmdlet migrates a reserved IP address to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="c8f1e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8f1e-111">EXAMPLES</span></span>

### <span data-ttu-id="c8f1e-112">1:</span><span class="sxs-lookup"><span data-stu-id="c8f1e-112">1:</span></span>
```

```

## <span data-ttu-id="c8f1e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8f1e-113">PARAMETERS</span></span>

### <span data-ttu-id="c8f1e-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="c8f1e-114">-Abort</span></span>
<span data-ttu-id="c8f1e-115">Indica che questo cmdlet Annulla la migrazione degli indirizzi IP riservati.</span><span class="sxs-lookup"><span data-stu-id="c8f1e-115">Indicates that this cmdlet cancels the reserved IP address migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f1e-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="c8f1e-116">-Commit</span></span>
<span data-ttu-id="c8f1e-117">Indica che questo cmdlet avvia la migrazione degli indirizzi IP riservati.</span><span class="sxs-lookup"><span data-stu-id="c8f1e-117">Indicates that this cmdlet starts the reserved IP address migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f1e-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c8f1e-118">-InformationAction</span></span>
<span data-ttu-id="c8f1e-119">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c8f1e-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c8f1e-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c8f1e-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8f1e-121">Continuare</span><span class="sxs-lookup"><span data-stu-id="c8f1e-121">Continue</span></span>
- <span data-ttu-id="c8f1e-122">Ignora</span><span class="sxs-lookup"><span data-stu-id="c8f1e-122">Ignore</span></span>
- <span data-ttu-id="c8f1e-123">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c8f1e-123">Inquire</span></span>
- <span data-ttu-id="c8f1e-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c8f1e-124">SilentlyContinue</span></span>
- <span data-ttu-id="c8f1e-125">Stop</span><span class="sxs-lookup"><span data-stu-id="c8f1e-125">Stop</span></span>
- <span data-ttu-id="c8f1e-126">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c8f1e-126">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f1e-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c8f1e-127">-InformationVariable</span></span>
<span data-ttu-id="c8f1e-128">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c8f1e-128">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f1e-129">-Preparare</span><span class="sxs-lookup"><span data-stu-id="c8f1e-129">-Prepare</span></span>
<span data-ttu-id="c8f1e-130">Indica che questo cmdlet prepara l'indirizzo IP riservato per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="c8f1e-130">Indicates that this cmdlet prepares the reserved IP address for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f1e-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="c8f1e-131">-Profile</span></span>
<span data-ttu-id="c8f1e-132">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8f1e-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c8f1e-133">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c8f1e-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f1e-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="c8f1e-134">-ReservedIPName</span></span>
<span data-ttu-id="c8f1e-135">Specifica il nome dell'indirizzo IP riservato che viene migrato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8f1e-135">Specifies the name of the reserved IP address that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="c8f1e-136">-Convalida</span><span class="sxs-lookup"><span data-stu-id="c8f1e-136">-Validate</span></span>
<span data-ttu-id="c8f1e-137">Specifica che questo cmdlet convalida l'indirizzo IP riservato per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="c8f1e-137">Specifies that this cmdlet validates the reserved IP address for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f1e-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c8f1e-138">-Confirm</span></span>
<span data-ttu-id="c8f1e-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8f1e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8f1e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8f1e-140">-WhatIf</span></span>
<span data-ttu-id="c8f1e-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8f1e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8f1e-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8f1e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8f1e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f1e-143">CommonParameters</span></span>
<span data-ttu-id="c8f1e-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8f1e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f1e-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8f1e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f1e-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8f1e-146">INPUTS</span></span>

## <span data-ttu-id="c8f1e-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8f1e-147">OUTPUTS</span></span>

## <span data-ttu-id="c8f1e-148">Note</span><span class="sxs-lookup"><span data-stu-id="c8f1e-148">NOTES</span></span>

## <span data-ttu-id="c8f1e-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8f1e-149">RELATED LINKS</span></span>

[<span data-ttu-id="c8f1e-150">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c8f1e-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="c8f1e-151">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8f1e-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="c8f1e-152">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="c8f1e-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="c8f1e-153">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8f1e-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="c8f1e-154">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c8f1e-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


