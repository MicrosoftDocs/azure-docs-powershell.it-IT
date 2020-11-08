---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6DFD49F-26A5-4199-A844-CA0FC405BEDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9fc407e2cf7375708fe82253f3d2fb40eb78f60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029659"
---
# <span data-ttu-id="3c85f-101">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="3c85f-101">New-AzureVMConfig</span></span>

## <span data-ttu-id="3c85f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c85f-102">SYNOPSIS</span></span>
<span data-ttu-id="3c85f-103">Crea un oggetto di configurazione della macchina virtuale Azure.</span><span class="sxs-lookup"><span data-stu-id="3c85f-103">Creates an Azure virtual machine configuration object.</span></span>

## <span data-ttu-id="3c85f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c85f-104">SYNTAX</span></span>

### <span data-ttu-id="3c85f-105">ImageName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c85f-105">ImageName (Default)</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-ImageName] <String> [[-MediaLocation] <String>]
 [[-DiskLabel] <String>] [-DisableBootDiagnostics] [-LicenseType <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3c85f-106">DiskName</span><span class="sxs-lookup"><span data-stu-id="3c85f-106">DiskName</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-DiskName] <String> [-DisableBootDiagnostics]
 [-LicenseType <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3c85f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c85f-107">DESCRIPTION</span></span>
<span data-ttu-id="3c85f-108">Il cmdlet **New-AzureVMConfig** crea un oggetto di configurazione di una macchina virtuale Azure.</span><span class="sxs-lookup"><span data-stu-id="3c85f-108">The **New-AzureVMConfig** cmdlet creates an Azure  virtual machine configuration object.</span></span>
<span data-ttu-id="3c85f-109">Puoi usare questo oggetto per eseguire una nuova distribuzione e aggiungere una nuova macchina virtuale a una distribuzione esistente.</span><span class="sxs-lookup"><span data-stu-id="3c85f-109">You can use this object to perform a new deployment and add a new virtual machine to an existing deployment.</span></span>

## <span data-ttu-id="3c85f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c85f-110">EXAMPLES</span></span>

### <span data-ttu-id="3c85f-111">Esempio 1: creare una configurazione di una macchina virtuale Windows</span><span class="sxs-lookup"><span data-stu-id="3c85f-111">Example 1: Create a Windows virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[4].ImageName 
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Windows -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="3c85f-112">Questo comando crea una configurazione di una macchina virtuale Windows con il disco del sistema operativo, il disco di dati e la configurazione del provisioning.</span><span class="sxs-lookup"><span data-stu-id="3c85f-112">This command creates a Windows virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="3c85f-113">Questa configurazione viene quindi usata per creare una nuova macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3c85f-113">This configuration is then used to create a new virtual machine.</span></span>

### <span data-ttu-id="3c85f-114">Esempio 2: creare una configurazione di una macchina virtuale Linux</span><span class="sxs-lookup"><span data-stu-id="3c85f-114">Example 2: Create a Linux virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[7].ImageName
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Linux -LinuxUser $LinuxUser -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="3c85f-115">Questo comando crea una nuova configurazione della macchina virtuale Linux con il disco del sistema operativo, il disco di dati e la configurazione di provisioning.</span><span class="sxs-lookup"><span data-stu-id="3c85f-115">This command creates a new Linux virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="3c85f-116">Questa configurazione viene quindi usata per creare una nuova macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3c85f-116">This configuration is then used to create a new virtual machine.</span></span>

## <span data-ttu-id="3c85f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c85f-117">PARAMETERS</span></span>

### <span data-ttu-id="3c85f-118">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="3c85f-118">-AvailabilitySetName</span></span>
<span data-ttu-id="3c85f-119">Specifica il nome del set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="3c85f-119">Specifies the name of the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c85f-120">-DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3c85f-120">-DisableBootDiagnostics</span></span>
<span data-ttu-id="3c85f-121">Indica che la configurazione Disabilita la diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="3c85f-121">Indicates that the configuration disables boot diagnostics.</span></span>
<span data-ttu-id="3c85f-122">Per impostazione predefinita, la diagnostica di avvio è abilitata nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3c85f-122">By default, boot diagnostics are enabled on the virtual machine.</span></span>

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

### <span data-ttu-id="3c85f-123">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="3c85f-123">-DiskLabel</span></span>
<span data-ttu-id="3c85f-124">Specifica un'etichetta per il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3c85f-124">Specifies a label for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c85f-125">-Diskname</span><span class="sxs-lookup"><span data-stu-id="3c85f-125">-DiskName</span></span>
<span data-ttu-id="3c85f-126">Specifica un nome per il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3c85f-126">Specifies a name for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: DiskName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c85f-127">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="3c85f-127">-HostCaching</span></span>
<span data-ttu-id="3c85f-128">Specifica la modalità di memorizzazione nella cache ospitante per il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3c85f-128">Specifies the host caching mode for the operating system disk.</span></span>

<span data-ttu-id="3c85f-129">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="3c85f-129">Valid values are:</span></span>

- <span data-ttu-id="3c85f-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3c85f-130">ReadOnly</span></span>
- <span data-ttu-id="3c85f-131">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3c85f-131">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c85f-132">-ImageName</span><span class="sxs-lookup"><span data-stu-id="3c85f-132">-ImageName</span></span>
<span data-ttu-id="3c85f-133">Specifica il nome dell'immagine della macchina virtuale da usare per il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3c85f-133">Specifies the name of the virtual machine image to use for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c85f-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3c85f-134">-InformationAction</span></span>
<span data-ttu-id="3c85f-135">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="3c85f-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3c85f-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3c85f-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3c85f-137">Continuare</span><span class="sxs-lookup"><span data-stu-id="3c85f-137">Continue</span></span>
- <span data-ttu-id="3c85f-138">Ignora</span><span class="sxs-lookup"><span data-stu-id="3c85f-138">Ignore</span></span>
- <span data-ttu-id="3c85f-139">Informarsi</span><span class="sxs-lookup"><span data-stu-id="3c85f-139">Inquire</span></span>
- <span data-ttu-id="3c85f-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3c85f-140">SilentlyContinue</span></span>
- <span data-ttu-id="3c85f-141">Stop</span><span class="sxs-lookup"><span data-stu-id="3c85f-141">Stop</span></span>
- <span data-ttu-id="3c85f-142">Sospensione</span><span class="sxs-lookup"><span data-stu-id="3c85f-142">Suspend</span></span>

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

### <span data-ttu-id="3c85f-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3c85f-143">-InformationVariable</span></span>
<span data-ttu-id="3c85f-144">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="3c85f-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3c85f-145">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="3c85f-145">-InstanceSize</span></span>
<span data-ttu-id="3c85f-146">Specifica le dimensioni dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="3c85f-146">Specifies the size of the instance.</span></span>

<span data-ttu-id="3c85f-147">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3c85f-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3c85f-148">Dimensioni minime</span><span class="sxs-lookup"><span data-stu-id="3c85f-148">ExtraSmall</span></span>
- <span data-ttu-id="3c85f-149">Small</span><span class="sxs-lookup"><span data-stu-id="3c85f-149">Small</span></span>
- <span data-ttu-id="3c85f-150">Medio</span><span class="sxs-lookup"><span data-stu-id="3c85f-150">Medium</span></span>
- <span data-ttu-id="3c85f-151">Grande</span><span class="sxs-lookup"><span data-stu-id="3c85f-151">Large</span></span>
- <span data-ttu-id="3c85f-152">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="3c85f-152">ExtraLarge</span></span>
- <span data-ttu-id="3c85f-153">A5</span><span class="sxs-lookup"><span data-stu-id="3c85f-153">A5</span></span>
- <span data-ttu-id="3c85f-154">A6</span><span class="sxs-lookup"><span data-stu-id="3c85f-154">A6</span></span>
- <span data-ttu-id="3c85f-155">A7</span><span class="sxs-lookup"><span data-stu-id="3c85f-155">A7</span></span>
- <span data-ttu-id="3c85f-156">A8</span><span class="sxs-lookup"><span data-stu-id="3c85f-156">A8</span></span>
- <span data-ttu-id="3c85f-157">A9</span><span class="sxs-lookup"><span data-stu-id="3c85f-157">A9</span></span>
- <span data-ttu-id="3c85f-158">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="3c85f-158">Basic_A0</span></span>
- <span data-ttu-id="3c85f-159">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="3c85f-159">Basic_A1</span></span>
- <span data-ttu-id="3c85f-160">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="3c85f-160">Basic_A2</span></span>
- <span data-ttu-id="3c85f-161">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="3c85f-161">Basic_A3</span></span>
- <span data-ttu-id="3c85f-162">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="3c85f-162">Basic_A4</span></span>
- <span data-ttu-id="3c85f-163">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="3c85f-163">Standard_D1</span></span>
- <span data-ttu-id="3c85f-164">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="3c85f-164">Standard_D2</span></span>
- <span data-ttu-id="3c85f-165">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="3c85f-165">Standard_D3</span></span>
- <span data-ttu-id="3c85f-166">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="3c85f-166">Standard_D4</span></span>
- <span data-ttu-id="3c85f-167">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="3c85f-167">Standard_D11</span></span>
- <span data-ttu-id="3c85f-168">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="3c85f-168">Standard_D12</span></span>
- <span data-ttu-id="3c85f-169">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="3c85f-169">Standard_D13</span></span>
- <span data-ttu-id="3c85f-170">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="3c85f-170">Standard_D14</span></span>

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

### <span data-ttu-id="3c85f-171">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="3c85f-171">-Label</span></span>
<span data-ttu-id="3c85f-172">Specifica un'etichetta da assegnare alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3c85f-172">Specifies a label to assign to the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c85f-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3c85f-173">-LicenseType</span></span>
<span data-ttu-id="3c85f-174">Specifica il tipo di licenza per un'immagine o un disco concesso in licenza locale.</span><span class="sxs-lookup"><span data-stu-id="3c85f-174">Specifies the type of license for an image or disk that is licensed on-premises.</span></span>
<span data-ttu-id="3c85f-175">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3c85f-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3c85f-176">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="3c85f-176">Windows_Client</span></span>
- <span data-ttu-id="3c85f-177">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="3c85f-177">Windows_Server</span></span> 

<span data-ttu-id="3c85f-178">Specifica questo parametro solo per le immagini che contengono il sistema operativo Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c85f-178">Specify this parameter only for images that contain the Windows Server operating system.</span></span>

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

### <span data-ttu-id="3c85f-179">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="3c85f-179">-MediaLocation</span></span>
<span data-ttu-id="3c85f-180">Specifica la posizione di archiviazione di Azure per il nuovo disco della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3c85f-180">Specifies the Azure storage location for the new virtual machine disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c85f-181">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c85f-181">-Name</span></span>
<span data-ttu-id="3c85f-182">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3c85f-182">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="3c85f-183">-Profile</span><span class="sxs-lookup"><span data-stu-id="3c85f-183">-Profile</span></span>
<span data-ttu-id="3c85f-184">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c85f-184">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3c85f-185">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3c85f-185">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3c85f-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c85f-186">CommonParameters</span></span>
<span data-ttu-id="3c85f-187">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c85f-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c85f-188">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c85f-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c85f-189">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c85f-189">INPUTS</span></span>

## <span data-ttu-id="3c85f-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c85f-190">OUTPUTS</span></span>

## <span data-ttu-id="3c85f-191">Note</span><span class="sxs-lookup"><span data-stu-id="3c85f-191">NOTES</span></span>

## <span data-ttu-id="3c85f-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c85f-192">RELATED LINKS</span></span>

