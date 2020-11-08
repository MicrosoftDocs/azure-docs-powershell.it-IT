---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8418A93-8E6B-4A1C-B319-7CACE95AB600
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1daf0cb8881beeb71f0b3fe68732d596c56ce12
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029702"
---
# <span data-ttu-id="413ff-101">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="413ff-101">Move-AzureService</span></span>

## <span data-ttu-id="413ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="413ff-102">SYNOPSIS</span></span>
<span data-ttu-id="413ff-103">Esegue la migrazione di un servizio cloud allo stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="413ff-103">Migrates a cloud service to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="413ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="413ff-104">SYNTAX</span></span>

### <span data-ttu-id="413ff-105">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="413ff-105">AbortMigrationParameterSet</span></span>
```
Move-AzureService [-Abort] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="413ff-106">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="413ff-106">CommitMigrationParameterSet</span></span>
```
Move-AzureService [-Commit] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="413ff-107">PrepareNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="413ff-107">PrepareNewMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="413ff-108">PrepareExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="413ff-108">PrepareExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="413ff-109">ValidateNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="413ff-109">ValidateNewMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="413ff-110">ValidateExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="413ff-110">ValidateExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="413ff-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="413ff-111">DESCRIPTION</span></span>
<span data-ttu-id="413ff-112">Il cmdlet **Move-AzureService** esegue la migrazione di un servizio cloud e di una distribuzione all'interno di tale servizio a un gruppo di risorse nello stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="413ff-112">The **Move-AzureService** cmdlet migrates a cloud service and a deployment inside that service to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="413ff-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="413ff-113">EXAMPLES</span></span>

### <span data-ttu-id="413ff-114">Esempio 1: preparare la migrazione del servizio</span><span class="sxs-lookup"><span data-stu-id="413ff-114">Example 1: Prepare service migration</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="413ff-115">Questo comando prepara il servizio denominato ContosoService per la migrazione allo stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="413ff-115">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="413ff-116">La migrazione include la distribuzione denominata ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="413ff-116">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="413ff-117">Esempio 2: avviare la migrazione del servizio</span><span class="sxs-lookup"><span data-stu-id="413ff-117">Example 2: Start service migration</span></span>
```
PS C:\> Move-AzureService -Commit -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="413ff-118">Questo comando avvia la migrazione del servizio denominato ContosoService allo stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="413ff-118">This command starts migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="413ff-119">La migrazione include la distribuzione denominata ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="413ff-119">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="413ff-120">Esempio 3: annullare la migrazione del servizio</span><span class="sxs-lookup"><span data-stu-id="413ff-120">Example 3: Cancel service migration</span></span>
```
PS C:\> Move-AzureService -Abort -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="413ff-121">Questo comando Annulla la migrazione del servizio denominato ContosoService allo stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="413ff-121">This command cancels migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="413ff-122">Esempio 4: preparare la migrazione del servizio a una rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="413ff-122">Example 4: Prepare service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "VnetRG" -VirtualNetworkName "ContosoVNET" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="413ff-123">Questo comando prepara il servizio denominato ContosoService per la migrazione allo stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="413ff-123">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="413ff-124">La migrazione include la distribuzione denominata ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="413ff-124">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="413ff-125">La migrazione usa una rete virtuale creata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="413ff-125">The migration uses a virtual network that was previously created.</span></span>

### <span data-ttu-id="413ff-126">Esempio 5: convalidare la migrazione del servizio</span><span class="sxs-lookup"><span data-stu-id="413ff-126">Example 5: Validate service migration</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="413ff-127">Questo comando convalida la migrazione per il servizio denominato ContosoService nello stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="413ff-127">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="413ff-128">La migrazione include la distribuzione denominata ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="413ff-128">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="413ff-129">Esempio 6: convalidare la migrazione del servizio a una rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="413ff-129">Example 6: Validate service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "contosoService" -DeploymentName "contosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "vnetRG" -VirtualNetworkName "contosoVNET" -SubnetName "contosoSubnet"
```

<span data-ttu-id="413ff-130">Questo comando convalida la migrazione per il servizio denominato ContosoService nello stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="413ff-130">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="413ff-131">La migrazione include la distribuzione denominata ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="413ff-131">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="413ff-132">La migrazione usa una rete virtuale creata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="413ff-132">The migration uses a virtual network that was previously created.</span></span>

## <span data-ttu-id="413ff-133">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="413ff-133">PARAMETERS</span></span>

### <span data-ttu-id="413ff-134">-Abort</span><span class="sxs-lookup"><span data-stu-id="413ff-134">-Abort</span></span>
<span data-ttu-id="413ff-135">Indica che questo cmdlet Annulla la migrazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="413ff-135">Indicates that this cmdlet cancels the service migration.</span></span>

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

### <span data-ttu-id="413ff-136">-Commit</span><span class="sxs-lookup"><span data-stu-id="413ff-136">-Commit</span></span>
<span data-ttu-id="413ff-137">Indica che il cmdlet avvia la migrazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="413ff-137">Indicates that this cmdlet starts the service migration.</span></span>

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

### <span data-ttu-id="413ff-138">-CreateNewVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="413ff-138">-CreateNewVirtualNetwork</span></span>
<span data-ttu-id="413ff-139">Indica che questo cmdlet crea una rete virtuale nello stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="413ff-139">Indicates that this cmdlet creates a virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, ValidateNewMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="413ff-140">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="413ff-140">-DeploymentName</span></span>
<span data-ttu-id="413ff-141">Specifica il nome della distribuzione del servizio cloud in cui viene eseguita la migrazione del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="413ff-141">Specifies the name of the cloud service deployment that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="413ff-142">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="413ff-142">-InformationAction</span></span>
<span data-ttu-id="413ff-143">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="413ff-143">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="413ff-144">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="413ff-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="413ff-145">Continuare</span><span class="sxs-lookup"><span data-stu-id="413ff-145">Continue</span></span>
- <span data-ttu-id="413ff-146">Ignora</span><span class="sxs-lookup"><span data-stu-id="413ff-146">Ignore</span></span>
- <span data-ttu-id="413ff-147">Informarsi</span><span class="sxs-lookup"><span data-stu-id="413ff-147">Inquire</span></span>
- <span data-ttu-id="413ff-148">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="413ff-148">SilentlyContinue</span></span>
- <span data-ttu-id="413ff-149">Stop</span><span class="sxs-lookup"><span data-stu-id="413ff-149">Stop</span></span>
- <span data-ttu-id="413ff-150">Sospensione</span><span class="sxs-lookup"><span data-stu-id="413ff-150">Suspend</span></span>

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

### <span data-ttu-id="413ff-151">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="413ff-151">-InformationVariable</span></span>
<span data-ttu-id="413ff-152">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="413ff-152">Specifies an information variable.</span></span>

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

### <span data-ttu-id="413ff-153">-Preparare</span><span class="sxs-lookup"><span data-stu-id="413ff-153">-Prepare</span></span>
<span data-ttu-id="413ff-154">Indica che questo cmdlet prepara il servizio cloud per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="413ff-154">Indicates that this cmdlet prepares the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, PrepareExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="413ff-155">-Profile</span><span class="sxs-lookup"><span data-stu-id="413ff-155">-Profile</span></span>
<span data-ttu-id="413ff-156">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="413ff-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="413ff-157">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="413ff-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="413ff-158">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="413ff-158">-ServiceName</span></span>
<span data-ttu-id="413ff-159">Specifica il nome del servizio cloud a cui viene eseguita la migrazione del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="413ff-159">Specifies the name  of the cloud service that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="413ff-160">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="413ff-160">-SubnetName</span></span>
<span data-ttu-id="413ff-161">Specifica il nome della subnet all'interno della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="413ff-161">Specifies the name of the Subnet inside the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="413ff-162">-UseExistingVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="413ff-162">-UseExistingVirtualNetwork</span></span>
<span data-ttu-id="413ff-163">Indica che questo cmdlet esegue la migrazione del servizio cloud in una rete virtuale esistente nello stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="413ff-163">Indicates that this cmdlet migrates the cloud service to an existing virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="413ff-164">-Convalida</span><span class="sxs-lookup"><span data-stu-id="413ff-164">-Validate</span></span>
<span data-ttu-id="413ff-165">Specifica che questo cmdlet convalida il servizio cloud per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="413ff-165">Specifies that this cmdlet validates the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateNewMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="413ff-166">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="413ff-166">-VirtualNetworkName</span></span>
<span data-ttu-id="413ff-167">Specifica il nome di una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="413ff-167">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="413ff-168">-VirtualNetworkResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="413ff-168">-VirtualNetworkResourceGroupName</span></span>
<span data-ttu-id="413ff-169">Specifica il nome del gruppo di risorse di una rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="413ff-169">Specifies the name of the resource group of an existing virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="413ff-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="413ff-170">CommonParameters</span></span>
<span data-ttu-id="413ff-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="413ff-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="413ff-172">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="413ff-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="413ff-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="413ff-173">INPUTS</span></span>

## <span data-ttu-id="413ff-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="413ff-174">OUTPUTS</span></span>

## <span data-ttu-id="413ff-175">Note</span><span class="sxs-lookup"><span data-stu-id="413ff-175">NOTES</span></span>

## <span data-ttu-id="413ff-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="413ff-176">RELATED LINKS</span></span>

[<span data-ttu-id="413ff-177">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="413ff-177">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="413ff-178">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="413ff-178">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="413ff-179">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="413ff-179">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="413ff-180">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="413ff-180">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="413ff-181">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="413ff-181">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


