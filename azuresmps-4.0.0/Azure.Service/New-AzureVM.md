---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1999C880-F8F9-4CED-91A9-33E9BBDFE27D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09a3d7be7bf71e73443dcbb31464ee6f7f19b43a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029662"
---
# <span data-ttu-id="95867-101">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="95867-101">New-AzureVM</span></span>

## <span data-ttu-id="95867-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95867-102">SYNOPSIS</span></span>
<span data-ttu-id="95867-103">Crea una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="95867-103">Creates an Azure virtual machine.</span></span>

## <span data-ttu-id="95867-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95867-104">SYNTAX</span></span>

### <span data-ttu-id="95867-105">ExistingService (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="95867-105">ExistingService (Default)</span></span>
```
New-AzureVM -ServiceName <String> [-DeploymentLabel <String>] [-DeploymentName <String>] [-VNetName <String>]
 [-DnsSettings <DnsServer[]>] [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]>
 [-WaitForBoot] [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="95867-106">CreateService</span><span class="sxs-lookup"><span data-stu-id="95867-106">CreateService</span></span>
```
New-AzureVM -ServiceName <String> [-Location <String>] [-AffinityGroup <String>] [-ServiceLabel <String>]
 [-ReverseDnsFqdn <String>] [-ServiceDescription <String>] [-DeploymentLabel <String>]
 [-DeploymentName <String>] [-VNetName <String>] [-DnsSettings <DnsServer[]>]
 [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]> [-WaitForBoot]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="95867-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95867-107">DESCRIPTION</span></span>
<span data-ttu-id="95867-108">Il cmdlet **New-AzureVM** aggiunge una nuova macchina virtuale a un servizio Azure esistente oppure crea una macchina virtuale e un servizio nell'abbonamento corrente se è specificata la *posizione* o *AffinityGroup* .</span><span class="sxs-lookup"><span data-stu-id="95867-108">The **New-AzureVM** cmdlet adds a new virtual machine to an existing Azure service, or creates a virtual machine and service in the current subscription if either the *Location* or *AffinityGroup* is specified.</span></span>

## <span data-ttu-id="95867-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95867-109">EXAMPLES</span></span>

### <span data-ttu-id="95867-110">Esempio 1: creare una macchina virtuale per una configurazione di Windows</span><span class="sxs-lookup"><span data-stu-id="95867-110">Example 1: Create a virtual machine for a Windows configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine07" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername PsTestAdmin | New-AzureVM -ServiceName "ContosoService" -AffinityGroup "Contoso" -WaitForBoot
```

<span data-ttu-id="95867-111">Questo comando crea una configurazione di provisioning basata su una configurazione della macchina virtuale per il sistema operativo Windows e la usa per creare una macchina virtuale in un gruppo di affinità specificato.</span><span class="sxs-lookup"><span data-stu-id="95867-111">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="95867-112">Esempio 2: creare una macchina virtuale per una configurazione Linux</span><span class="sxs-lookup"><span data-stu-id="95867-112">Example 2: Create a virtual machine for a Linux configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "SUSEVM02" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[7].ImageName | Add-AzureProvisioningConfig -Linux -LinuxUser "RootMain" -Password "password" -AdminUsername PsTestAdmin | New-AzureVM
```

<span data-ttu-id="95867-113">Questo comando crea una configurazione di provisioning basata su una configurazione della macchina virtuale per Linux e la usa per creare una macchina virtuale in un gruppo di affinità specificato.</span><span class="sxs-lookup"><span data-stu-id="95867-113">This command creates a provisioning configuration based on a virtual machine configuration for Linux, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="95867-114">Esempio 3: creare una macchina virtuale e aggiungere un disco di dati</span><span class="sxs-lookup"><span data-stu-id="95867-114">Example 3: Create a virtual machine and add a data disk</span></span>
```
PS C:\> $Images = Get-AzureVMImage
PS C:\> $Image = $Images[4]
PS C:\> $VirtualMachine02 = New-AzureVMConfig -Name "VirtualMachine02" -InstanceSize ExtraSmall -ImageName $myImage.ImageName | Add-AzureProvisioningConfig -Windows -Password "password" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "DataDisk50" -LUN 0
```

<span data-ttu-id="95867-115">I primi due comandi ottengono le immagini disponibili usando il cmdlet **Get-AzureVMImage** e ne archiviano uno nella variabile $Image.</span><span class="sxs-lookup"><span data-stu-id="95867-115">The first two commands get available images by using the **Get-AzureVMImage** cmdlet, and stores one of them in the $Image variable.</span></span>

<span data-ttu-id="95867-116">Questo comando crea una configurazione di provisioning basata su una configurazione della macchina virtuale per il sistema operativo Windows e la usa per creare una macchina virtuale con un disco di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="95867-116">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with an Azure data disk.</span></span>

### <span data-ttu-id="95867-117">Esempio 4: creare una macchina virtuale con un indirizzo IP riservato</span><span class="sxs-lookup"><span data-stu-id="95867-117">Example 4: Create a virtual machine with a reserved IP address</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine06" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService02" -AffinityGroup "Contoso" -ReservedIPName $ipName
```

<span data-ttu-id="95867-118">Questo comando crea una configurazione di provisioning basata su una configurazione della macchina virtuale per il sistema operativo Windows e la usa per creare una macchina virtuale con un indirizzo IP riservato.</span><span class="sxs-lookup"><span data-stu-id="95867-118">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with a reserved IP address.</span></span>

## <span data-ttu-id="95867-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95867-119">PARAMETERS</span></span>

### <span data-ttu-id="95867-120">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="95867-120">-AffinityGroup</span></span>
<span data-ttu-id="95867-121">Specifica il gruppo di affinità di Azure in cui risiede il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="95867-121">Specifies the Azure affinity group in which the cloud service resides.</span></span>
<span data-ttu-id="95867-122">Questo parametro è obbligatorio solo quando questo cmdlet crea un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="95867-122">This parameter is required only when this cmdlet creates a cloud service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95867-123">-DeploymentLabel</span><span class="sxs-lookup"><span data-stu-id="95867-123">-DeploymentLabel</span></span>
<span data-ttu-id="95867-124">Specifica un'etichetta per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="95867-124">Specifies a label for the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95867-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="95867-125">-DeploymentName</span></span>
<span data-ttu-id="95867-126">Specifica un nome di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="95867-126">Specifies a deployment name.</span></span>
<span data-ttu-id="95867-127">Se non specificato, questo cmdlet usa il nome del servizio come nome di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="95867-127">If not specified, this cmdlet uses the service name as the deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95867-128">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="95867-128">-DnsSettings</span></span>
<span data-ttu-id="95867-129">Specifica un oggetto server DNS che definisce le impostazioni DNS per la nuova distribuzione.</span><span class="sxs-lookup"><span data-stu-id="95867-129">Specifies a DNS Server object that defines the DNS settings for the new deployment.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95867-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="95867-130">-InformationAction</span></span>
<span data-ttu-id="95867-131">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="95867-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="95867-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="95867-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="95867-133">Continuare</span><span class="sxs-lookup"><span data-stu-id="95867-133">Continue</span></span>
- <span data-ttu-id="95867-134">Ignora</span><span class="sxs-lookup"><span data-stu-id="95867-134">Ignore</span></span>
- <span data-ttu-id="95867-135">Informarsi</span><span class="sxs-lookup"><span data-stu-id="95867-135">Inquire</span></span>
- <span data-ttu-id="95867-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="95867-136">SilentlyContinue</span></span>
- <span data-ttu-id="95867-137">Stop</span><span class="sxs-lookup"><span data-stu-id="95867-137">Stop</span></span>
- <span data-ttu-id="95867-138">Sospensione</span><span class="sxs-lookup"><span data-stu-id="95867-138">Suspend</span></span>

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

### <span data-ttu-id="95867-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="95867-139">-InformationVariable</span></span>
<span data-ttu-id="95867-140">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="95867-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="95867-141">-InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="95867-141">-InternalLoadBalancerConfig</span></span>
<span data-ttu-id="95867-142">Specifica un bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="95867-142">Specifies an internal load balancer.</span></span>
<span data-ttu-id="95867-143">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="95867-143">This parameter is not used.</span></span>

```yaml
Type: InternalLoadBalancerConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95867-144">-Posizione</span><span class="sxs-lookup"><span data-stu-id="95867-144">-Location</span></span>
<span data-ttu-id="95867-145">Specifica la posizione che ospita il nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="95867-145">Specifies the location that hosts the new service.</span></span>
<span data-ttu-id="95867-146">Se il servizio esiste già, non specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="95867-146">If the service already exists, do not specify this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95867-147">-Profile</span><span class="sxs-lookup"><span data-stu-id="95867-147">-Profile</span></span>
<span data-ttu-id="95867-148">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95867-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="95867-149">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="95867-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="95867-150">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="95867-150">-ReservedIPName</span></span>
<span data-ttu-id="95867-151">Specifica il nome dell'indirizzo IP riservato.</span><span class="sxs-lookup"><span data-stu-id="95867-151">Specifies the name of the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95867-152">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="95867-152">-ReverseDnsFqdn</span></span>
<span data-ttu-id="95867-153">Specifica il nome di dominio completo per il DNS inverso.</span><span class="sxs-lookup"><span data-stu-id="95867-153">Specifies the fully-qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95867-154">-ServiceDescription</span><span class="sxs-lookup"><span data-stu-id="95867-154">-ServiceDescription</span></span>
<span data-ttu-id="95867-155">Specifica una descrizione per il nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="95867-155">Specifies a description for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95867-156">-ServiceLabel</span><span class="sxs-lookup"><span data-stu-id="95867-156">-ServiceLabel</span></span>
<span data-ttu-id="95867-157">Specifica un'etichetta per il nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="95867-157">Specifies a label for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95867-158">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="95867-158">-ServiceName</span></span>
<span data-ttu-id="95867-159">Specifica il nome del servizio nuovo o esistente.</span><span class="sxs-lookup"><span data-stu-id="95867-159">Specifies the new or existing service name.</span></span>

<span data-ttu-id="95867-160">Se il servizio non esiste, questo cmdlet lo crea automaticamente.</span><span class="sxs-lookup"><span data-stu-id="95867-160">If the service does not exist, this cmdlet creates it for you.</span></span>
<span data-ttu-id="95867-161">Usa il parametro *location* o *AffinityGroup* per specificare dove creare il servizio.</span><span class="sxs-lookup"><span data-stu-id="95867-161">Use the *Location* or *AffinityGroup* parameter to specify where to create the service.</span></span>

<span data-ttu-id="95867-162">Se il servizio esiste, il parametro *location* o *AffinityGroup* non è necessario.</span><span class="sxs-lookup"><span data-stu-id="95867-162">If the service exists, the *Location* or *AffinityGroup* parameter is not needed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95867-163">-VM</span><span class="sxs-lookup"><span data-stu-id="95867-163">-VMs</span></span>
<span data-ttu-id="95867-164">Specifica un elenco di oggetti macchina virtuale da creare.</span><span class="sxs-lookup"><span data-stu-id="95867-164">Specifies a list of virtual machine objects to create.</span></span>

```yaml
Type: PersistentVM[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95867-165">-VNetName</span><span class="sxs-lookup"><span data-stu-id="95867-165">-VNetName</span></span>
<span data-ttu-id="95867-166">Specifica il nome della rete virtuale in cui questo cmdlet distribuisce la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="95867-166">Specifies the virtual network name where this cmdlet deploys the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95867-167">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="95867-167">-WaitForBoot</span></span>
<span data-ttu-id="95867-168">Specifica che questo cmdlet attende che la macchina virtuale raggiunga lo stato **ReadyRole** .</span><span class="sxs-lookup"><span data-stu-id="95867-168">Specifies that this cmdlet waits for the virtual machine to reach the **ReadyRole** state.</span></span>
<span data-ttu-id="95867-169">Questo cmdlet non riesce se la macchina virtuale rientra in uno degli Stati seguenti in attesa: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="95867-169">This cmdlet fails if the virtual machine falls in one of the following states while waiting: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span></span>

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

### <span data-ttu-id="95867-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95867-170">CommonParameters</span></span>
<span data-ttu-id="95867-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95867-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95867-172">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95867-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95867-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95867-173">INPUTS</span></span>

## <span data-ttu-id="95867-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95867-174">OUTPUTS</span></span>

## <span data-ttu-id="95867-175">Note</span><span class="sxs-lookup"><span data-stu-id="95867-175">NOTES</span></span>

## <span data-ttu-id="95867-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95867-176">RELATED LINKS</span></span>

[<span data-ttu-id="95867-177">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="95867-177">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="95867-178">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="95867-178">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="95867-179">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="95867-179">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="95867-180">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="95867-180">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)


