---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023867"
---
# <span data-ttu-id="7f120-101">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="7f120-101">New-AzureQuickVM</span></span>

## <span data-ttu-id="7f120-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f120-102">SYNOPSIS</span></span>
<span data-ttu-id="7f120-103">Configura e crea una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="7f120-103">Configures and creates an Azure virtual machine.</span></span>

## <span data-ttu-id="7f120-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f120-104">SYNTAX</span></span>

### <span data-ttu-id="7f120-105">Windows (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f120-105">Windows (Default)</span></span>
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7f120-106">Linux</span><span class="sxs-lookup"><span data-stu-id="7f120-106">Linux</span></span>
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7f120-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f120-107">DESCRIPTION</span></span>
<span data-ttu-id="7f120-108">Il cmdlet **New-AzureQuickVM** configura e crea una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="7f120-108">The **New-AzureQuickVM** cmdlet configures and creates an Azure virtual machine.</span></span>
<span data-ttu-id="7f120-109">Questo cmdlet può distribuire una macchina virtuale in un servizio Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="7f120-109">This cmdlet can deploy a virtual machine into an existing Azure service.</span></span>
<span data-ttu-id="7f120-110">Questo cmdlet può in alternativa creare un servizio Azure che ospita la nuova macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f120-110">This cmdlet can alternatively create an Azure service that hosts the new virtual machine.</span></span>

## <span data-ttu-id="7f120-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f120-111">EXAMPLES</span></span>

### <span data-ttu-id="7f120-112">Esempio 1: creare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="7f120-112">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

<span data-ttu-id="7f120-113">Questo comando crea una macchina virtuale che esegue il sistema operativo Windows in un servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="7f120-113">This command creates a virtual machine that runs the Windows operating system in an existing service.</span></span>
<span data-ttu-id="7f120-114">Il cmdlet basa la macchina virtuale sull'immagine specificata.</span><span class="sxs-lookup"><span data-stu-id="7f120-114">The cmdlet bases the virtual machine on the specified image.</span></span>
<span data-ttu-id="7f120-115">Il comando specifica il parametro *WaitForBoot* .</span><span class="sxs-lookup"><span data-stu-id="7f120-115">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="7f120-116">Di conseguenza, il cmdlet attende che la macchina virtuale venga avviata.</span><span class="sxs-lookup"><span data-stu-id="7f120-116">Therefore, the cmdlet waits for the virtual machine to start.</span></span>

### <span data-ttu-id="7f120-117">Esempio 2: creare una macchina virtuale usando i certificati</span><span class="sxs-lookup"><span data-stu-id="7f120-117">Example 2: Create a virtual machine that by using certificates</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

<span data-ttu-id="7f120-118">Il primo comando ottiene i certificati da un archivio e li archivia nella variabile $certs.</span><span class="sxs-lookup"><span data-stu-id="7f120-118">The first command gets certificates from a store, and stores them in the $certs variable.</span></span>

<span data-ttu-id="7f120-119">Il secondo comando crea una macchina virtuale che esegue il sistema operativo Windows in un servizio esistente da un'immagine.</span><span class="sxs-lookup"><span data-stu-id="7f120-119">The second command creates a virtual machine that runs the Windows operating system in an existing service from an image.</span></span>
<span data-ttu-id="7f120-120">Per impostazione predefinita, il listener HTTPS di WinRM è abilitato nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f120-120">By default, WinRM Https listener is enabled on the virtual machine.</span></span>
<span data-ttu-id="7f120-121">Il comando specifica il parametro *WaitForBoot* .</span><span class="sxs-lookup"><span data-stu-id="7f120-121">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="7f120-122">Di conseguenza, il cmdlet attende che la macchina virtuale venga avviata.</span><span class="sxs-lookup"><span data-stu-id="7f120-122">Therefore, the cmdlet waits for the virtual machine to start.</span></span>
<span data-ttu-id="7f120-123">Il comando carica un certificato WinRM e X509Certificates nel servizio ospitato.</span><span class="sxs-lookup"><span data-stu-id="7f120-123">The command uploads a WinRM Certificate and X509Certificates to the hosted service.</span></span>

### <span data-ttu-id="7f120-124">Esempio 3: creare una macchina virtuale che esegue il sistema operativo Linux</span><span class="sxs-lookup"><span data-stu-id="7f120-124">Example 3: Create a virtual machine that runs the Linux operating system</span></span>
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

<span data-ttu-id="7f120-125">Questo comando crea una macchina virtuale che esegue il sistema operativo Linux da un'immagine.</span><span class="sxs-lookup"><span data-stu-id="7f120-125">This command creates a virtual machine that runs the Linux operating system from an image.</span></span>
<span data-ttu-id="7f120-126">Questo comando crea un servizio per ospitare la nuova macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f120-126">This command creates a service to host the new virtual machine.</span></span>
<span data-ttu-id="7f120-127">Il comando specifica una posizione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="7f120-127">The command specifies a location for the service.</span></span>

### <span data-ttu-id="7f120-128">Esempio 4: creare una macchina virtuale e creare un servizio per ospitare la nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="7f120-128">Example 4: Create a virtual machine and create a service to host the new virtual machine</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

<span data-ttu-id="7f120-129">Il primo comando ottiene i percorsi usando il cmdlet **Get-AzureLocation** e li archivia nella variabile di matrice $locations.</span><span class="sxs-lookup"><span data-stu-id="7f120-129">The first command gets locations by using the **Get-AzureLocation** cmdlet, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="7f120-130">Il secondo comando ottiene le immagini disponibili usando il cmdlet **Get-AzureVMImage** e li archivia nella variabile di matrice $images.</span><span class="sxs-lookup"><span data-stu-id="7f120-130">The second command gets available images by using the **Get-AzureVMImage** cmdlet, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="7f120-131">Il comando finale crea una grande macchina virtuale denominata VirtualMachine25.</span><span class="sxs-lookup"><span data-stu-id="7f120-131">The final command creates a large virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="7f120-132">La macchina virtuale esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="7f120-132">The virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="7f120-133">Si basa su una delle immagini in $Images.</span><span class="sxs-lookup"><span data-stu-id="7f120-133">It is based on one of the images in $Images.</span></span>
<span data-ttu-id="7f120-134">Il comando crea un servizio denominato ContosoService03 per la nuova macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f120-134">The command creates a service named ContosoService03 for the new virtual machine.</span></span>
<span data-ttu-id="7f120-135">Il servizio si trova in una posizione in $Locations.</span><span class="sxs-lookup"><span data-stu-id="7f120-135">The service is in a location in $Locations.</span></span>

### <span data-ttu-id="7f120-136">Esempio 5: creare una macchina virtuale con un nome IP riservato</span><span class="sxs-lookup"><span data-stu-id="7f120-136">Example 5: Create a virtual machine that has a reserved IP name</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

<span data-ttu-id="7f120-137">Il primo comando ottiene i percorsi e li archivia nella variabile di matrice $Locations.</span><span class="sxs-lookup"><span data-stu-id="7f120-137">The first command gets locations, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="7f120-138">Il secondo comando consente di ottenere le immagini disponibili e quindi di archiviarle nella variabile di matrice $Images.</span><span class="sxs-lookup"><span data-stu-id="7f120-138">The second command gets available images, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="7f120-139">Il comando finale crea una macchina virtuale denominata VirtualMachine27 in base a una delle immagini in $Images.</span><span class="sxs-lookup"><span data-stu-id="7f120-139">The final command creates a virtual machine named VirtualMachine27 based on one of the images in $Images.</span></span>
<span data-ttu-id="7f120-140">Il comando crea un servizio in una posizione in $Locations.</span><span class="sxs-lookup"><span data-stu-id="7f120-140">The command creates a service in a location in $Locations.</span></span>
<span data-ttu-id="7f120-141">La macchina virtuale ha un nome IP riservato, memorizzato in precedenza nella variabile $ipName.</span><span class="sxs-lookup"><span data-stu-id="7f120-141">The virtual machine has a reserved IP name, previously stored in the $ipName variable.</span></span>

## <span data-ttu-id="7f120-142">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f120-142">PARAMETERS</span></span>

### <span data-ttu-id="7f120-143">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="7f120-143">-AdminUsername</span></span>
<span data-ttu-id="7f120-144">Specifica il nome utente dell'account di amministratore creato da questo cmdlet nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f120-144">Specifies the user name of the Administrator account that this cmdlet creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-145">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="7f120-145">-AffinityGroup</span></span>
<span data-ttu-id="7f120-146">Specifica il gruppo affinità per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f120-146">Specifies the affinity group for the virtual machine.</span></span>
<span data-ttu-id="7f120-147">Specifica questo parametro o il parametro *location* solo se questo cmdlet crea un servizio Azure per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f120-147">Specify this parameter or the *Location* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

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

### <span data-ttu-id="7f120-148">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="7f120-148">-AvailabilitySetName</span></span>
<span data-ttu-id="7f120-149">Specifica il nome del set di disponibilità in cui questo cmdlet crea la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f120-149">Specifies the name of the availability set in which this cmdlet creates the virtual machine.</span></span>

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

### <span data-ttu-id="7f120-150">-Certificati</span><span class="sxs-lookup"><span data-stu-id="7f120-150">-Certificates</span></span>
<span data-ttu-id="7f120-151">Specifica un elenco di certificati usati da questo cmdlet per creare il servizio.</span><span class="sxs-lookup"><span data-stu-id="7f120-151">Specifies a list of certificates that this cmdlet uses to create the service.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-152">-CustomDataFile</span><span class="sxs-lookup"><span data-stu-id="7f120-152">-CustomDataFile</span></span>
<span data-ttu-id="7f120-153">Specifica un file di dati per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f120-153">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="7f120-154">Questo cmdlet codifica il contenuto del file come Base64.</span><span class="sxs-lookup"><span data-stu-id="7f120-154">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="7f120-155">Il file deve essere di lunghezza inferiore a 64 kilobyte.</span><span class="sxs-lookup"><span data-stu-id="7f120-155">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="7f120-156">Se il sistema operativo guest è il sistema operativo Windows, questo cmdlet salva questi dati come file binario denominato%SYSTEMDRIVE%\AzureData\CustomData.bin.</span><span class="sxs-lookup"><span data-stu-id="7f120-156">If the guest operating system is the Windows operating system, this cmdlet saves this data as a binary file that is named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="7f120-157">Se il sistema operativo guest è Linux, questo cmdlet passa i dati usando il file ovf-env.xml.</span><span class="sxs-lookup"><span data-stu-id="7f120-157">If the guest operating system is Linux, this cmdlet passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="7f120-158">L'installazione copia il file nella directory/var/lib/waagent.</span><span class="sxs-lookup"><span data-stu-id="7f120-158">Installation copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="7f120-159">L'agente archivia anche i dati codificati base64 in/var/lib/waagent/CustomData.</span><span class="sxs-lookup"><span data-stu-id="7f120-159">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

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

### <span data-ttu-id="7f120-160">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="7f120-160">-DisableGuestAgent</span></span>
<span data-ttu-id="7f120-161">Indica che questo cmdlet disabilita l'agente guest per il provisioning dell'infrastruttura come servizio (IaaS).</span><span class="sxs-lookup"><span data-stu-id="7f120-161">Indicates that this cmdlet disables the infrastructure as a service (IaaS) provision guest agent.</span></span>

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

### <span data-ttu-id="7f120-162">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="7f120-162">-DisableWinRMHttps</span></span>
<span data-ttu-id="7f120-163">Indica che questo cmdlet disabilita la gestione remota di Windows in HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7f120-163">Indicates that this cmdlet disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="7f120-164">Per impostazione predefinita, WinRM è abilitato su HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7f120-164">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-165">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="7f120-165">-DnsSettings</span></span>
<span data-ttu-id="7f120-166">Specifica una matrice di oggetti server DNS che definisce le impostazioni DNS per la nuova distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7f120-166">Specifies an array of DNS server objects that defines the DNS settings for the new deployment.</span></span>
<span data-ttu-id="7f120-167">Per creare un oggetto **dnsserver** , usa il cmdlet **New-AzureDns** .</span><span class="sxs-lookup"><span data-stu-id="7f120-167">To create a **DnsServer** object, use the **New-AzureDns** cmdlet.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-168">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="7f120-168">-EnableWinRMHttp</span></span>
<span data-ttu-id="7f120-169">Indica che questo cmdlet Abilita WinRM tramite HTTP.</span><span class="sxs-lookup"><span data-stu-id="7f120-169">Indicates that this cmdlet enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-170">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="7f120-170">-HostCaching</span></span>
<span data-ttu-id="7f120-171">Specifica la modalità di memorizzazione nella cache ospitante per il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7f120-171">Specifies the host caching mode for the operating system disk.</span></span>
<span data-ttu-id="7f120-172">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="7f120-172">Valid values are:</span></span> 

- <span data-ttu-id="7f120-173">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="7f120-173">ReadOnly</span></span>
- <span data-ttu-id="7f120-174">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7f120-174">ReadWrite</span></span>

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

### <span data-ttu-id="7f120-175">-ImageName</span><span class="sxs-lookup"><span data-stu-id="7f120-175">-ImageName</span></span>
<span data-ttu-id="7f120-176">Specifica il nome dell'immagine del disco utilizzata dal cmdlet per creare il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7f120-176">Specifies the name of the disk image this cmdlet uses to create the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-177">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7f120-177">-InformationAction</span></span>
<span data-ttu-id="7f120-178">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="7f120-178">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7f120-179">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f120-179">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f120-180">Continuare</span><span class="sxs-lookup"><span data-stu-id="7f120-180">Continue</span></span>
- <span data-ttu-id="7f120-181">Ignora</span><span class="sxs-lookup"><span data-stu-id="7f120-181">Ignore</span></span>
- <span data-ttu-id="7f120-182">Informarsi</span><span class="sxs-lookup"><span data-stu-id="7f120-182">Inquire</span></span>
- <span data-ttu-id="7f120-183">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7f120-183">SilentlyContinue</span></span>
- <span data-ttu-id="7f120-184">Stop</span><span class="sxs-lookup"><span data-stu-id="7f120-184">Stop</span></span>
- <span data-ttu-id="7f120-185">Sospensione</span><span class="sxs-lookup"><span data-stu-id="7f120-185">Suspend</span></span>

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

### <span data-ttu-id="7f120-186">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7f120-186">-InformationVariable</span></span>
<span data-ttu-id="7f120-187">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="7f120-187">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7f120-188">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="7f120-188">-InstanceSize</span></span>
<span data-ttu-id="7f120-189">Specifica le dimensioni dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7f120-189">Specifies the size of the instance.</span></span>
<span data-ttu-id="7f120-190">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="7f120-190">Valid values are:</span></span> 

- <span data-ttu-id="7f120-191">Dimensioni minime</span><span class="sxs-lookup"><span data-stu-id="7f120-191">ExtraSmall</span></span>
- <span data-ttu-id="7f120-192">Small</span><span class="sxs-lookup"><span data-stu-id="7f120-192">Small</span></span>
- <span data-ttu-id="7f120-193">Medio</span><span class="sxs-lookup"><span data-stu-id="7f120-193">Medium</span></span>
- <span data-ttu-id="7f120-194">Grande</span><span class="sxs-lookup"><span data-stu-id="7f120-194">Large</span></span>
- <span data-ttu-id="7f120-195">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="7f120-195">ExtraLarge</span></span>
- <span data-ttu-id="7f120-196">A5</span><span class="sxs-lookup"><span data-stu-id="7f120-196">A5</span></span>
- <span data-ttu-id="7f120-197">A6</span><span class="sxs-lookup"><span data-stu-id="7f120-197">A6</span></span>
- <span data-ttu-id="7f120-198">A7</span><span class="sxs-lookup"><span data-stu-id="7f120-198">A7</span></span>
- <span data-ttu-id="7f120-199">A8</span><span class="sxs-lookup"><span data-stu-id="7f120-199">A8</span></span>
- <span data-ttu-id="7f120-200">A9</span><span class="sxs-lookup"><span data-stu-id="7f120-200">A9</span></span>
- <span data-ttu-id="7f120-201">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="7f120-201">Basic_A0</span></span>
- <span data-ttu-id="7f120-202">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="7f120-202">Basic_A1</span></span>
- <span data-ttu-id="7f120-203">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="7f120-203">Basic_A2</span></span>
- <span data-ttu-id="7f120-204">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="7f120-204">Basic_A3</span></span>
- <span data-ttu-id="7f120-205">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="7f120-205">Basic_A4</span></span>
- <span data-ttu-id="7f120-206">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="7f120-206">Standard_D1</span></span>
- <span data-ttu-id="7f120-207">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="7f120-207">Standard_D2</span></span>
- <span data-ttu-id="7f120-208">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="7f120-208">Standard_D3</span></span>
- <span data-ttu-id="7f120-209">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="7f120-209">Standard_D4</span></span>
- <span data-ttu-id="7f120-210">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="7f120-210">Standard_D11</span></span>
- <span data-ttu-id="7f120-211">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="7f120-211">Standard_D12</span></span>
- <span data-ttu-id="7f120-212">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="7f120-212">Standard_D13</span></span>
- <span data-ttu-id="7f120-213">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="7f120-213">Standard_D14</span></span>

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

### <span data-ttu-id="7f120-214">-Linux</span><span class="sxs-lookup"><span data-stu-id="7f120-214">-Linux</span></span>
<span data-ttu-id="7f120-215">Indica che questo cmdlet crea una macchina virtuale basata su Linux.</span><span class="sxs-lookup"><span data-stu-id="7f120-215">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-216">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="7f120-216">-LinuxUser</span></span>
<span data-ttu-id="7f120-217">Specifica il nome utente dell'account amministrativo di Linux creato da questo cmdlet nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f120-217">Specifies the user name of the Linux administrative account that this cmdlet creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-218">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7f120-218">-Location</span></span>
<span data-ttu-id="7f120-219">Specifica il Data Center di Azure che ospita la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f120-219">Specifies the Azure datacenter that hosts the virtual machine.</span></span>
<span data-ttu-id="7f120-220">Se specifichi questo parametro, il cmdlet crea un servizio Azure nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="7f120-220">If you specify this parameter, the cmdlet creates an Azure service in the specified location.</span></span>
<span data-ttu-id="7f120-221">Specifica questo parametro o il parametro *AffinityGroup* solo se questo cmdlet crea un servizio Azure per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f120-221">Specify this parameter or the *AffinityGroup* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

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

### <span data-ttu-id="7f120-222">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="7f120-222">-MediaLocation</span></span>
<span data-ttu-id="7f120-223">Specifica il percorso di archiviazione di Azure in cui questo cmdlet crea i dischi delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="7f120-223">Specifies the Azure Storage location where this cmdlet creates the virtual machines disks.</span></span>

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

### <span data-ttu-id="7f120-224">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f120-224">-Name</span></span>
<span data-ttu-id="7f120-225">Specifica il nome della macchina virtuale creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f120-225">Specifies the name of the virtual machine that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7f120-226">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="7f120-226">-NoExportPrivateKey</span></span>
<span data-ttu-id="7f120-227">Indica che questa configurazione non carica la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="7f120-227">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-228">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f120-228">-NoWinRMEndpoint</span></span>
<span data-ttu-id="7f120-229">Indica che questo cmdlet non aggiunge un endpoint di WinRM per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f120-229">Indicates that this cmdlet does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-230">-Password</span><span class="sxs-lookup"><span data-stu-id="7f120-230">-Password</span></span>
<span data-ttu-id="7f120-231">Specifica la password per l'account amministrativo.</span><span class="sxs-lookup"><span data-stu-id="7f120-231">Specifies the password for the administrative account.</span></span>

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

### <span data-ttu-id="7f120-232">-Profile</span><span class="sxs-lookup"><span data-stu-id="7f120-232">-Profile</span></span>
<span data-ttu-id="7f120-233">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f120-233">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7f120-234">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="7f120-234">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7f120-235">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="7f120-235">-ReservedIPName</span></span>
<span data-ttu-id="7f120-236">Specifica il nome IP riservato.</span><span class="sxs-lookup"><span data-stu-id="7f120-236">Specifies the reserved IP name.</span></span>

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

### <span data-ttu-id="7f120-237">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="7f120-237">-ReverseDnsFqdn</span></span>
<span data-ttu-id="7f120-238">Specifica il nome di dominio completo per la ricerca di DNS inverso.</span><span class="sxs-lookup"><span data-stu-id="7f120-238">Specifies the fully qualified domain name for reverse DNS look up.</span></span>

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

### <span data-ttu-id="7f120-239">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7f120-239">-ServiceName</span></span>
<span data-ttu-id="7f120-240">Specifica il nome di un servizio Azure nuovo o esistente a cui questo cmdlet aggiunge la nuova macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f120-240">Specifies the name of a new or existing Azure service to which this cmdlet adds the new virtual machine.</span></span>

<span data-ttu-id="7f120-241">Se specifichi un nuovo servizio, questo cmdlet la crea.</span><span class="sxs-lookup"><span data-stu-id="7f120-241">If you specify a new service, this cmdlets creates it.</span></span>
<span data-ttu-id="7f120-242">Per creare un nuovo servizio, devi specificare il *percorso* o il parametro *AffinityGroup* .</span><span class="sxs-lookup"><span data-stu-id="7f120-242">To create a new service, you must specify the *Location* or *AffinityGroup* parameter.</span></span>

<span data-ttu-id="7f120-243">Se specifichi un servizio esistente, non specificare la *posizione* o *AffinityGroup*.</span><span class="sxs-lookup"><span data-stu-id="7f120-243">If you specify an existing service, do not specify *Location* or *AffinityGroup*.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-244">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="7f120-244">-SSHKeyPairs</span></span>
<span data-ttu-id="7f120-245">Specifica le coppie di chiavi SSH.</span><span class="sxs-lookup"><span data-stu-id="7f120-245">Specifies SSH key pairs.</span></span>

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-246">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="7f120-246">-SSHPublicKeys</span></span>
<span data-ttu-id="7f120-247">Specifica le chiavi pubbliche di SSH.</span><span class="sxs-lookup"><span data-stu-id="7f120-247">Specifies SSH public keys.</span></span>

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-248">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="7f120-248">-SubnetNames</span></span>
<span data-ttu-id="7f120-249">Specifica una matrice di nomi di subnet per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f120-249">Specifies an array of names of subnet for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-250">-VNetName</span><span class="sxs-lookup"><span data-stu-id="7f120-250">-VNetName</span></span>
<span data-ttu-id="7f120-251">Specifica il nome di una rete virtuale per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f120-251">Specifies the name of a virtual network for the virtual machine.</span></span>

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

### <span data-ttu-id="7f120-252">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="7f120-252">-WaitForBoot</span></span>
<span data-ttu-id="7f120-253">Indica che questo cmdlet attende che la macchina virtuale raggiunga lo stato ReadyRole.</span><span class="sxs-lookup"><span data-stu-id="7f120-253">Indicates that this cmdlet waits for the virtual machine to reach the state ReadyRole.</span></span>
<span data-ttu-id="7f120-254">Se la macchina virtuale raggiunge uno degli Stati seguenti, il cmdlet non riesce: FailedStartingVM, ProvisioningFailed o ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="7f120-254">If the virtual machine reaches one of the following states, the cmdlet fails: FailedStartingVM, ProvisioningFailed, or ProvisioningTimeout.</span></span>

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

### <span data-ttu-id="7f120-255">-Windows</span><span class="sxs-lookup"><span data-stu-id="7f120-255">-Windows</span></span>
<span data-ttu-id="7f120-256">Indica che questo cmdlet crea una macchina virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="7f120-256">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-257">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="7f120-257">-WinRMCertificate</span></span>
<span data-ttu-id="7f120-258">Specifica un certificato associato a un endpoint di WinRM da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f120-258">Specifies a certificate that this cmdlet associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-259">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="7f120-259">-X509Certificates</span></span>
<span data-ttu-id="7f120-260">Specifica una matrice di certificati X509 distribuiti in un servizio ospitato.</span><span class="sxs-lookup"><span data-stu-id="7f120-260">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f120-261">CommonParameters</span></span>
<span data-ttu-id="7f120-262">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f120-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f120-263">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f120-263">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f120-264">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f120-264">INPUTS</span></span>

## <span data-ttu-id="7f120-265">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f120-265">OUTPUTS</span></span>

## <span data-ttu-id="7f120-266">Note</span><span class="sxs-lookup"><span data-stu-id="7f120-266">NOTES</span></span>

## <span data-ttu-id="7f120-267">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f120-267">RELATED LINKS</span></span>

[<span data-ttu-id="7f120-268">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="7f120-268">Get-AzureLocation</span></span>](./Get-AzureLocation.md)

[<span data-ttu-id="7f120-269">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7f120-269">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="7f120-270">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="7f120-270">New-AzureDns</span></span>](./New-AzureDns.md)


