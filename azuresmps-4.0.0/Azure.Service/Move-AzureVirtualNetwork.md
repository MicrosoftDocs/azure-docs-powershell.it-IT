---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2B0CC65A-0A73-4FFE-BF7C-B148871909D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: df768878bf26c186751171edf7ed41acb3f7d15a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029700"
---
# <span data-ttu-id="b4bf9-101">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b4bf9-101">Move-AzureVirtualNetwork</span></span>

## <span data-ttu-id="b4bf9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="b4bf9-103">Esegue la migrazione di una rete virtuale allo stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-103">Migrates a virtual network to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="b4bf9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4bf9-104">SYNTAX</span></span>

### <span data-ttu-id="b4bf9-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4bf9-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4bf9-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4bf9-106">AbortMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4bf9-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4bf9-107">CommitMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4bf9-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4bf9-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4bf9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4bf9-109">DESCRIPTION</span></span>
<span data-ttu-id="b4bf9-110">Il cmdlet **Move-AzureVirtualNetwork** esegue la migrazione di una rete virtuale a un gruppo di risorse nello stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-110">The **Move-AzureVirtualNetwork** cmdlet migrates a virtual network to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="b4bf9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4bf9-111">EXAMPLES</span></span>

### <span data-ttu-id="b4bf9-112">Esempio 1: preparare la migrazione della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="b4bf9-112">Example 1: Prepare virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Prepare -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="b4bf9-113">Questo comando prepara la rete virtuale denominata ContosoVNET per la migrazione allo stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-113">This command prepares the virtual network named ContosoVNET for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="b4bf9-114">Esempio 2: avviare la migrazione della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="b4bf9-114">Example 2: Start virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Commit -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="b4bf9-115">Questo comando avvia la migrazione della rete virtuale denominata ContosoVNET allo stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-115">This command starts migration of the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="b4bf9-116">Esempio 3: convalidare la migrazione della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="b4bf9-116">Example 3: Validate virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Validate -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="b4bf9-117">Questo comando convalida la migrazione per la rete virtuale denominata ContosoVNET nello stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-117">This command validates migration for the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="b4bf9-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4bf9-118">PARAMETERS</span></span>

### <span data-ttu-id="b4bf9-119">-Abort</span><span class="sxs-lookup"><span data-stu-id="b4bf9-119">-Abort</span></span>
<span data-ttu-id="b4bf9-120">Indica che questo cmdlet Annulla la migrazione della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-120">Indicates that this cmdlet cancels the virtual network migration.</span></span>

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

### <span data-ttu-id="b4bf9-121">-Commit</span><span class="sxs-lookup"><span data-stu-id="b4bf9-121">-Commit</span></span>
<span data-ttu-id="b4bf9-122">Indica che questo cmdlet avvia la migrazione della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-122">Indicates that this cmdlet starts the virtual network migration.</span></span>

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

### <span data-ttu-id="b4bf9-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b4bf9-123">-InformationAction</span></span>
<span data-ttu-id="b4bf9-124">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b4bf9-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b4bf9-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4bf9-126">Continuare</span><span class="sxs-lookup"><span data-stu-id="b4bf9-126">Continue</span></span>
- <span data-ttu-id="b4bf9-127">Ignora</span><span class="sxs-lookup"><span data-stu-id="b4bf9-127">Ignore</span></span>
- <span data-ttu-id="b4bf9-128">Informarsi</span><span class="sxs-lookup"><span data-stu-id="b4bf9-128">Inquire</span></span>
- <span data-ttu-id="b4bf9-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b4bf9-129">SilentlyContinue</span></span>
- <span data-ttu-id="b4bf9-130">Stop</span><span class="sxs-lookup"><span data-stu-id="b4bf9-130">Stop</span></span>
- <span data-ttu-id="b4bf9-131">Sospensione</span><span class="sxs-lookup"><span data-stu-id="b4bf9-131">Suspend</span></span>

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

### <span data-ttu-id="b4bf9-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b4bf9-132">-InformationVariable</span></span>
<span data-ttu-id="b4bf9-133">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b4bf9-134">-Preparare</span><span class="sxs-lookup"><span data-stu-id="b4bf9-134">-Prepare</span></span>
<span data-ttu-id="b4bf9-135">Indica che questo cmdlet prepara la rete virtuale per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-135">Indicates that this cmdlet prepares the virtual network for migration.</span></span>

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

### <span data-ttu-id="b4bf9-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="b4bf9-136">-Profile</span></span>
<span data-ttu-id="b4bf9-137">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4bf9-138">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4bf9-139">-Convalida</span><span class="sxs-lookup"><span data-stu-id="b4bf9-139">-Validate</span></span>
<span data-ttu-id="b4bf9-140">Specifica che questo cmdlet convalida la rete virtuale per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-140">Specifies that this cmdlet validates the virtual network for migration.</span></span>

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

### <span data-ttu-id="b4bf9-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b4bf9-141">-VirtualNetworkName</span></span>
<span data-ttu-id="b4bf9-142">Nome della rete virtuale di cui eseguire la migrazione</span><span class="sxs-lookup"><span data-stu-id="b4bf9-142">Name of the Virtual Network to migrate</span></span>

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

### <span data-ttu-id="b4bf9-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b4bf9-143">-Confirm</span></span>
<span data-ttu-id="b4bf9-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4bf9-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4bf9-145">-WhatIf</span></span>
<span data-ttu-id="b4bf9-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4bf9-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4bf9-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4bf9-148">CommonParameters</span></span>
<span data-ttu-id="b4bf9-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4bf9-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4bf9-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4bf9-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4bf9-151">INPUTS</span></span>

## <span data-ttu-id="b4bf9-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4bf9-152">OUTPUTS</span></span>

## <span data-ttu-id="b4bf9-153">Note</span><span class="sxs-lookup"><span data-stu-id="b4bf9-153">NOTES</span></span>

## <span data-ttu-id="b4bf9-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4bf9-154">RELATED LINKS</span></span>

[<span data-ttu-id="b4bf9-155">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b4bf9-155">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="b4bf9-156">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="b4bf9-156">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="b4bf9-157">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="b4bf9-157">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="b4bf9-158">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="b4bf9-158">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="b4bf9-159">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4bf9-159">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)


