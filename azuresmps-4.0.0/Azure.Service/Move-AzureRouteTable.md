---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 01213154-DD8A-412F-A23D-5D9D09BEFA3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0602015a63d28aecb498b0830619ea1560d6066
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029703"
---
# <span data-ttu-id="1acea-101">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="1acea-101">Move-AzureRouteTable</span></span>

## <span data-ttu-id="1acea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1acea-102">SYNOPSIS</span></span>
<span data-ttu-id="1acea-103">Esegue la migrazione di una tabella di route allo stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="1acea-103">Migrates a route table to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="1acea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1acea-104">SYNTAX</span></span>

### <span data-ttu-id="1acea-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="1acea-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1acea-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="1acea-106">AbortMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1acea-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="1acea-107">CommitMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1acea-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="1acea-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1acea-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1acea-109">DESCRIPTION</span></span>
<span data-ttu-id="1acea-110">Il cmdlet **Move-AzureRouteTable** esegue la migrazione di una tabella di route a un gruppo di risorse nello stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="1acea-110">The **Move-AzureRouteTable** cmdlet migrates a route table to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="1acea-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1acea-111">EXAMPLES</span></span>

### <span data-ttu-id="1acea-112">1:</span><span class="sxs-lookup"><span data-stu-id="1acea-112">1:</span></span>
```

```

## <span data-ttu-id="1acea-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1acea-113">PARAMETERS</span></span>

### <span data-ttu-id="1acea-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="1acea-114">-Abort</span></span>
<span data-ttu-id="1acea-115">Indica che questo cmdlet Annulla la migrazione della tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="1acea-115">Indicates that this cmdlet cancels the route table migration.</span></span>

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

### <span data-ttu-id="1acea-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="1acea-116">-Commit</span></span>
<span data-ttu-id="1acea-117">Indica che il cmdlet avvia la migrazione della tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="1acea-117">Indicates that this cmdlet starts the route table migration.</span></span>

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

### <span data-ttu-id="1acea-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1acea-118">-InformationAction</span></span>
<span data-ttu-id="1acea-119">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="1acea-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1acea-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1acea-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1acea-121">Continuare</span><span class="sxs-lookup"><span data-stu-id="1acea-121">Continue</span></span>
- <span data-ttu-id="1acea-122">Ignora</span><span class="sxs-lookup"><span data-stu-id="1acea-122">Ignore</span></span>
- <span data-ttu-id="1acea-123">Informarsi</span><span class="sxs-lookup"><span data-stu-id="1acea-123">Inquire</span></span>
- <span data-ttu-id="1acea-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1acea-124">SilentlyContinue</span></span>
- <span data-ttu-id="1acea-125">Stop</span><span class="sxs-lookup"><span data-stu-id="1acea-125">Stop</span></span>
- <span data-ttu-id="1acea-126">Sospensione</span><span class="sxs-lookup"><span data-stu-id="1acea-126">Suspend</span></span>

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

### <span data-ttu-id="1acea-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1acea-127">-InformationVariable</span></span>
<span data-ttu-id="1acea-128">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="1acea-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1acea-129">-Preparare</span><span class="sxs-lookup"><span data-stu-id="1acea-129">-Prepare</span></span>
<span data-ttu-id="1acea-130">Indica che questo cmdlet prepara la tabella di route per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="1acea-130">Indicates that this cmdlet prepares the route table for migration.</span></span>

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

### <span data-ttu-id="1acea-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="1acea-131">-Profile</span></span>
<span data-ttu-id="1acea-132">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1acea-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1acea-133">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1acea-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1acea-134">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="1acea-134">-RouteTableName</span></span>
<span data-ttu-id="1acea-135">Specifica il nome della tabella di route migrata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1acea-135">Specifies the name of the route table that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="1acea-136">-Convalida</span><span class="sxs-lookup"><span data-stu-id="1acea-136">-Validate</span></span>
<span data-ttu-id="1acea-137">Specifica che questo cmdlet convalida la tabella di route per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="1acea-137">Specifies that this cmdlet validates the route table for migration.</span></span>

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

### <span data-ttu-id="1acea-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1acea-138">-Confirm</span></span>
<span data-ttu-id="1acea-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1acea-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1acea-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1acea-140">-WhatIf</span></span>
<span data-ttu-id="1acea-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1acea-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1acea-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1acea-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1acea-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1acea-143">CommonParameters</span></span>
<span data-ttu-id="1acea-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1acea-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1acea-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1acea-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1acea-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1acea-146">INPUTS</span></span>

## <span data-ttu-id="1acea-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1acea-147">OUTPUTS</span></span>

## <span data-ttu-id="1acea-148">Note</span><span class="sxs-lookup"><span data-stu-id="1acea-148">NOTES</span></span>

## <span data-ttu-id="1acea-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1acea-149">RELATED LINKS</span></span>

[<span data-ttu-id="1acea-150">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1acea-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="1acea-151">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="1acea-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="1acea-152">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="1acea-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="1acea-153">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1acea-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="1acea-154">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1acea-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


