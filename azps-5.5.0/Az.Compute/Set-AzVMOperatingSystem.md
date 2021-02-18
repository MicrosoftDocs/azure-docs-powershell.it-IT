---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204714"
---
# <span data-ttu-id="b86e3-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b86e3-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="b86e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b86e3-102">SYNOPSIS</span></span>
<span data-ttu-id="b86e3-103">Imposta le proprietà del sistema operativo per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b86e3-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="b86e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b86e3-104">SYNTAX</span></span>

### <span data-ttu-id="b86e3-105">Windows (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b86e3-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b86e3-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="b86e3-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b86e3-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="b86e3-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b86e3-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="b86e3-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b86e3-109">Linux</span><span class="sxs-lookup"><span data-stu-id="b86e3-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b86e3-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b86e3-110">DESCRIPTION</span></span>
<span data-ttu-id="b86e3-111">Il cmdlet **Set-AzVMOperatingSystem** imposta le proprietà del sistema operativo per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b86e3-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="b86e3-112">È possibile specificare le credenziali di accesso, il nome del computer e il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b86e3-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="b86e3-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b86e3-113">EXAMPLES</span></span>

### <span data-ttu-id="b86e3-114">Esempio 1: Impostare le proprietà del sistema operativo per una nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="b86e3-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="b86e3-115">Il primo comando converte una password in una stringa sicura e quindi la archivia nella $SecurePassword variabile.</span><span class="sxs-lookup"><span data-stu-id="b86e3-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="b86e3-116">Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="b86e3-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="b86e3-117">Il secondo comando crea le credenziali per l'utente FullerP e la password archiviate in $SecurePassword, quindi archivia le credenziali nella variabile $Credential utente.</span><span class="sxs-lookup"><span data-stu-id="b86e3-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="b86e3-118">Per altre informazioni, digitare `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="b86e3-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="b86e3-119">Il terzo comando ottiene il set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia l'oggetto nella $AvailabilitySet locale.</span><span class="sxs-lookup"><span data-stu-id="b86e3-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="b86e3-120">Il quarto comando crea un oggetto macchina virtuale e quindi lo archivia nella $VirtualMachine variabile.</span><span class="sxs-lookup"><span data-stu-id="b86e3-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b86e3-121">Il comando assegna un nome e le dimensioni alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b86e3-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b86e3-122">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="b86e3-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="b86e3-123">I quattro comandi seguenti assegnano valori alle variabili da usare nel comando seguente.</span><span class="sxs-lookup"><span data-stu-id="b86e3-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="b86e3-124">Queste stringhe possono essere specificate direttamente nel comando **Set-AzVMOperatingSystem,** quindi questo approccio viene usato solo per la leggibilità.</span><span class="sxs-lookup"><span data-stu-id="b86e3-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="b86e3-125">Tuttavia, è possibile usare un approccio come questo negli script.</span><span class="sxs-lookup"><span data-stu-id="b86e3-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="b86e3-126">Il comando finale imposta le proprietà del sistema operativo per la macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b86e3-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b86e3-127">Il comando usa le credenziali archiviate in $Credential.</span><span class="sxs-lookup"><span data-stu-id="b86e3-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="b86e3-128">Per alcuni parametri il comando usa le variabili assegnate nei comandi precedenti.</span><span class="sxs-lookup"><span data-stu-id="b86e3-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="b86e3-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b86e3-129">PARAMETERS</span></span>

### <span data-ttu-id="b86e3-130">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="b86e3-130">-ComputerName</span></span>
<span data-ttu-id="b86e3-131">Specifica il nome del computer.</span><span class="sxs-lookup"><span data-stu-id="b86e3-131">Specifies the name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86e3-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="b86e3-132">-Credential</span></span>
<span data-ttu-id="b86e3-133">Specifica il nome utente e la password della macchina virtuale come **oggetto PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="b86e3-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="b86e3-134">Per ottenere le credenziali, usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="b86e3-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="b86e3-135">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="b86e3-135">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86e3-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="b86e3-136">-CustomData</span></span>
<span data-ttu-id="b86e3-137">Specifica una stringa di dati personalizzati codificata in base 64.</span><span class="sxs-lookup"><span data-stu-id="b86e3-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="b86e3-138">Questa decodifica viene decodificata in una matrice binaria che viene salvata come file nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b86e3-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="b86e3-139">La lunghezza massima della matrice binaria è 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="b86e3-139">The maximum length of the binary array is 65535 bytes.</span></span><br>
<span data-ttu-id="b86e3-140">**Nota: non superare i segreti o le password nella proprietà customData**</span><span class="sxs-lookup"><span data-stu-id="b86e3-140">**Note: Do not pass any secrets or passwords in customData property**</span></span><br>
<span data-ttu-id="b86e3-141">Questa proprietà non può essere aggiornata dopo la creazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b86e3-141">This property cannot be updated after the VM is created.</span></span> <br>
<span data-ttu-id="b86e3-142">customData viene passato alla macchina virtuale per essere salvata come file. Per altre informazioni, vedere Dati personalizzati nelle [macchine virtuali di Azure](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span><span class="sxs-lookup"><span data-stu-id="b86e3-142">customData is passed to the VM to be saved as a file, for more information see [Custom Data on Azure VMs](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span></span> <br>
<span data-ttu-id="b86e3-143">Per l'uso di cloud-init per la macchina virtuale Linux, vedi Uso [di cloud-init](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init) per personalizzare una macchina virtuale Linux durante la creazione</span><span class="sxs-lookup"><span data-stu-id="b86e3-143">For using cloud-init for your Linux VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86e3-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b86e3-144">-DefaultProfile</span></span>
<span data-ttu-id="b86e3-145">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b86e3-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b86e3-146">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="b86e3-146">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="b86e3-147">Indica che questo cmdlet disabilita l'autenticazione tramite password.</span><span class="sxs-lookup"><span data-stu-id="b86e3-147">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86e3-148">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="b86e3-148">-DisableVMAgent</span></span>
<span data-ttu-id="b86e3-149">Disabilitare provisioning agente VM.</span><span class="sxs-lookup"><span data-stu-id="b86e3-149">Disable Provision VM Agent.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b86e3-150">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="b86e3-150">-EnableAutoUpdate</span></span>
<span data-ttu-id="b86e3-151">Indica che questo cmdlet abilita l'aggiornamento automatico.</span><span class="sxs-lookup"><span data-stu-id="b86e3-151">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86e3-152">-Linux</span><span class="sxs-lookup"><span data-stu-id="b86e3-152">-Linux</span></span>
<span data-ttu-id="b86e3-153">Indica che il tipo di sistema operativo è Linux.</span><span class="sxs-lookup"><span data-stu-id="b86e3-153">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86e3-154">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="b86e3-154">-PatchMode</span></span>
<span data-ttu-id="b86e3-155">Specifica la modalità di applicazione delle patch in-guest alla macchina virtuale IaaS.</span><span class="sxs-lookup"><span data-stu-id="b86e3-155">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="b86e3-156">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="b86e3-156">Possible values are:</span></span><br>
<span data-ttu-id="b86e3-157">**Manuale:** è possibile controllare l'applicazione delle patch a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b86e3-157">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="b86e3-158">A questo scopo, applicare manualmente le patch all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b86e3-158">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="b86e3-159">In questa modalità gli aggiornamenti automatici sono disabilitati; la proprietà WindowsConfiguration.enableAutomaticUpdates deve essere false</span><span class="sxs-lookup"><span data-stu-id="b86e3-159">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="b86e3-160">**AutomaticByOS:** la macchina virtuale verrà aggiornata automaticamente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b86e3-160">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="b86e3-161">La proprietà WindowsConfiguration.enableAutomaticUpdates deve essere true.</span><span class="sxs-lookup"><span data-stu-id="b86e3-161">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="b86e3-162">**AutomaticByPlatform:** la macchina virtuale verrà aggiornata automaticamente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b86e3-162">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="b86e3-163">Le proprietà provisionVMAgent e WindowsConfiguration.enableAutomaticUpdates devono essere true</span><span class="sxs-lookup"><span data-stu-id="b86e3-163">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86e3-164">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="b86e3-164">-ProvisionVMAgent</span></span>
<span data-ttu-id="b86e3-165">Indica che le impostazioni richiedono l'installazione dell'agente della macchina virtuale nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b86e3-165">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86e3-166">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="b86e3-166">-TimeZone</span></span>
<span data-ttu-id="b86e3-167">Specifica il fuso orario della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b86e3-167">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="b86e3-168">ad esempio Ora \" solare \" Pacifico.</span><span class="sxs-lookup"><span data-stu-id="b86e3-168">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="b86e3-169">I valori possibili possono essere [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) da fusi orari restituiti da [TimeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="b86e3-169">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86e3-170">-VM</span><span class="sxs-lookup"><span data-stu-id="b86e3-170">-VM</span></span>
<span data-ttu-id="b86e3-171">Specifica l'oggetto della macchina virtuale locale su cui impostare le proprietà del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b86e3-171">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="b86e3-172">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="b86e3-172">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="b86e3-173">Creare un oggetto macchina virtuale usando il cmdlet New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="b86e3-173">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b86e3-174">-Windows</span><span class="sxs-lookup"><span data-stu-id="b86e3-174">-Windows</span></span>
<span data-ttu-id="b86e3-175">Indica che il tipo di sistema operativo è Windows.</span><span class="sxs-lookup"><span data-stu-id="b86e3-175">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86e3-176">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="b86e3-176">-WinRMCertificateUrl</span></span>
<span data-ttu-id="b86e3-177">Specifica l'URI di un certificato WinRM.</span><span class="sxs-lookup"><span data-stu-id="b86e3-177">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="b86e3-178">Questa cartella deve essere archiviata in un Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="b86e3-178">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86e3-179">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="b86e3-179">-WinRMHttp</span></span>
<span data-ttu-id="b86e3-180">Indica che il sistema operativo usa HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="b86e3-180">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86e3-181">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="b86e3-181">-WinRMHttps</span></span>
<span data-ttu-id="b86e3-182">Indica che questo sistema operativo usa HTTPS WinRM.</span><span class="sxs-lookup"><span data-stu-id="b86e3-182">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86e3-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b86e3-183">CommonParameters</span></span>
<span data-ttu-id="b86e3-184">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b86e3-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b86e3-185">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b86e3-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b86e3-186">INPUT</span><span class="sxs-lookup"><span data-stu-id="b86e3-186">INPUTS</span></span>

### <span data-ttu-id="b86e3-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b86e3-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b86e3-188">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b86e3-188">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b86e3-189">System.String</span><span class="sxs-lookup"><span data-stu-id="b86e3-189">System.String</span></span>

### <span data-ttu-id="b86e3-190">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="b86e3-190">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="b86e3-191">System.Uri</span><span class="sxs-lookup"><span data-stu-id="b86e3-191">System.Uri</span></span>

## <span data-ttu-id="b86e3-192">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b86e3-192">OUTPUTS</span></span>

### <span data-ttu-id="b86e3-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b86e3-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b86e3-194">NOTE</span><span class="sxs-lookup"><span data-stu-id="b86e3-194">NOTES</span></span>

## <span data-ttu-id="b86e3-195">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b86e3-195">RELATED LINKS</span></span>

[<span data-ttu-id="b86e3-196">Get-AZVM</span><span class="sxs-lookup"><span data-stu-id="b86e3-196">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b86e3-197">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="b86e3-197">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


