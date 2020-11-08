---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 27ECCBAD-0CFE-4309-B590-BB60E1872ED5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d96f02374eb266cb9eaa3c1cc7c200a4f154043
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029705"
---
# <span data-ttu-id="a380b-101">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a380b-101">Move-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="a380b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a380b-102">SYNOPSIS</span></span>
<span data-ttu-id="a380b-103">Esegue la migrazione di un gruppo di sicurezza di rete allo stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="a380b-103">Migrates a Network Security Group to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="a380b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a380b-104">SYNTAX</span></span>

### <span data-ttu-id="a380b-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a380b-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a380b-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a380b-106">AbortMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a380b-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a380b-107">CommitMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a380b-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a380b-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a380b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a380b-109">DESCRIPTION</span></span>
<span data-ttu-id="a380b-110">Il cmdlet **Move-AzureNetworkSecurityGroup** esegue la migrazione di un gruppo di sicurezza di rete a un gruppo di risorse nello stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="a380b-110">The **Move-AzureNetworkSecurityGroup** cmdlet migrates a Network Security Group to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="a380b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a380b-111">EXAMPLES</span></span>

### <span data-ttu-id="a380b-112">1:</span><span class="sxs-lookup"><span data-stu-id="a380b-112">1:</span></span>
```

```

## <span data-ttu-id="a380b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a380b-113">PARAMETERS</span></span>

### <span data-ttu-id="a380b-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="a380b-114">-Abort</span></span>
<span data-ttu-id="a380b-115">Indica che questo cmdlet Annulla la migrazione del gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="a380b-115">Indicates that this cmdlet cancels the Network Security Group migration.</span></span>

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

### <span data-ttu-id="a380b-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="a380b-116">-Commit</span></span>
<span data-ttu-id="a380b-117">Indica che questo cmdlet avvia la migrazione dei gruppi di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="a380b-117">Indicates that this cmdlet starts the Network Security Group migration.</span></span>

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

### <span data-ttu-id="a380b-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a380b-118">-InformationAction</span></span>
<span data-ttu-id="a380b-119">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="a380b-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a380b-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a380b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a380b-121">Continuare</span><span class="sxs-lookup"><span data-stu-id="a380b-121">Continue</span></span>
- <span data-ttu-id="a380b-122">Ignora</span><span class="sxs-lookup"><span data-stu-id="a380b-122">Ignore</span></span>
- <span data-ttu-id="a380b-123">Informarsi</span><span class="sxs-lookup"><span data-stu-id="a380b-123">Inquire</span></span>
- <span data-ttu-id="a380b-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a380b-124">SilentlyContinue</span></span>
- <span data-ttu-id="a380b-125">Stop</span><span class="sxs-lookup"><span data-stu-id="a380b-125">Stop</span></span>
- <span data-ttu-id="a380b-126">Sospensione</span><span class="sxs-lookup"><span data-stu-id="a380b-126">Suspend</span></span>

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

### <span data-ttu-id="a380b-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a380b-127">-InformationVariable</span></span>
<span data-ttu-id="a380b-128">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="a380b-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a380b-129">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="a380b-129">-NetworkSecurityGroupName</span></span>
<span data-ttu-id="a380b-130">Specifica il nome del gruppo di sicurezza di rete a cui viene eseguita la migrazione del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a380b-130">Specifies the name of the Network Security Group that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="a380b-131">-Preparare</span><span class="sxs-lookup"><span data-stu-id="a380b-131">-Prepare</span></span>
<span data-ttu-id="a380b-132">Indica che questo cmdlet prepara il gruppo di sicurezza della rete per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="a380b-132">Indicates that this cmdlet prepares the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="a380b-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="a380b-133">-Profile</span></span>
<span data-ttu-id="a380b-134">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a380b-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a380b-135">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a380b-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a380b-136">-Convalida</span><span class="sxs-lookup"><span data-stu-id="a380b-136">-Validate</span></span>
<span data-ttu-id="a380b-137">Specifica che questo cmdlet convalida il gruppo di sicurezza della rete per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="a380b-137">Specifies that this cmdlet validates the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="a380b-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a380b-138">-Confirm</span></span>
<span data-ttu-id="a380b-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a380b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a380b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a380b-140">-WhatIf</span></span>
<span data-ttu-id="a380b-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a380b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a380b-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a380b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a380b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a380b-143">CommonParameters</span></span>
<span data-ttu-id="a380b-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a380b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a380b-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a380b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a380b-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a380b-146">INPUTS</span></span>

## <span data-ttu-id="a380b-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a380b-147">OUTPUTS</span></span>

## <span data-ttu-id="a380b-148">Note</span><span class="sxs-lookup"><span data-stu-id="a380b-148">NOTES</span></span>

## <span data-ttu-id="a380b-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a380b-149">RELATED LINKS</span></span>

[<span data-ttu-id="a380b-150">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="a380b-150">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="a380b-151">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="a380b-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="a380b-152">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="a380b-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="a380b-153">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a380b-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="a380b-154">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a380b-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


