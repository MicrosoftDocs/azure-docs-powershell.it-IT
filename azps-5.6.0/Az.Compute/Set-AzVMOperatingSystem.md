---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 75eb0ef60443cdbf2dfe3fa53202d3c8141d4888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990442"
---
# <span data-ttu-id="cdc42-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="cdc42-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="cdc42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdc42-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc42-103">Imposta le proprietà del sistema operativo per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cdc42-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="cdc42-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdc42-104">SYNTAX</span></span>

### <span data-ttu-id="cdc42-105">Windows (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cdc42-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdc42-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="cdc42-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdc42-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="cdc42-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdc42-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="cdc42-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdc42-109">Linux</span><span class="sxs-lookup"><span data-stu-id="cdc42-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-PatchMode <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdc42-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cdc42-110">DESCRIPTION</span></span>
<span data-ttu-id="cdc42-111">Il cmdlet **Set-AzVMOperatingSystem** imposta le proprietà del sistema operativo per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cdc42-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="cdc42-112">È possibile specificare le credenziali di accesso, il nome del computer e il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cdc42-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="cdc42-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdc42-113">EXAMPLES</span></span>

### <span data-ttu-id="cdc42-114">Esempio 1: Impostare le proprietà del sistema operativo per una nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="cdc42-114">Example 1: Set operating system properties for a new virtual machine</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="cdc42-115">Il primo comando converte una password in una stringa sicura e quindi la archivia nella $SecurePassword variabile.</span><span class="sxs-lookup"><span data-stu-id="cdc42-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="cdc42-116">Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="cdc42-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="cdc42-117">Il secondo comando crea le credenziali per l'utente FullerP e la password archiviate in $SecurePassword, quindi archivia le credenziali nella variabile $Credential utente.</span><span class="sxs-lookup"><span data-stu-id="cdc42-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="cdc42-118">Per altre informazioni, digitare `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="cdc42-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="cdc42-119">Il terzo comando ottiene il set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia l'oggetto nella $AvailabilitySet locale.</span><span class="sxs-lookup"><span data-stu-id="cdc42-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="cdc42-120">Il quarto comando crea un oggetto macchina virtuale e quindi lo archivia nella $VirtualMachine variabile.</span><span class="sxs-lookup"><span data-stu-id="cdc42-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="cdc42-121">Il comando assegna un nome e le dimensioni alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cdc42-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="cdc42-122">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="cdc42-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="cdc42-123">I quattro comandi seguenti assegnano valori alle variabili da usare nel comando seguente.</span><span class="sxs-lookup"><span data-stu-id="cdc42-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="cdc42-124">Queste stringhe possono essere specificate direttamente nel comando **Set-AzVMOperatingSystem,** quindi questo approccio viene usato solo per la leggibilità.</span><span class="sxs-lookup"><span data-stu-id="cdc42-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="cdc42-125">Tuttavia, è possibile usare un approccio come questo negli script.</span><span class="sxs-lookup"><span data-stu-id="cdc42-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="cdc42-126">Il comando finale imposta le proprietà del sistema operativo per la macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="cdc42-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="cdc42-127">Il comando usa le credenziali archiviate in $Credential.</span><span class="sxs-lookup"><span data-stu-id="cdc42-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="cdc42-128">Per alcuni parametri il comando usa le variabili assegnate nei comandi precedenti.</span><span class="sxs-lookup"><span data-stu-id="cdc42-128">The command uses variables assigned in previous commands for some parameters.</span></span>

### <span data-ttu-id="cdc42-129">Esempio 2: Impostare le proprietà del sistema operativo per una nuova macchina virtuale con le patch a scelta rapida abilitate</span><span class="sxs-lookup"><span data-stu-id="cdc42-129">Example 2: Set operating system properties for a new virtual machine with hot patching enabled</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform" -EnableHotPatching
```

<span data-ttu-id="cdc42-130">Il primo comando converte una password in una stringa sicura e quindi la archivia nella $SecurePassword variabile.</span><span class="sxs-lookup"><span data-stu-id="cdc42-130">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="cdc42-131">Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="cdc42-131">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="cdc42-132">Il secondo comando crea le credenziali per l'utente FullerP e la password archiviate in $SecurePassword, quindi archivia le credenziali nella variabile $Credential utente.</span><span class="sxs-lookup"><span data-stu-id="cdc42-132">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="cdc42-133">Per altre informazioni, digitare `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="cdc42-133">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="cdc42-134">Il terzo comando ottiene il set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia l'oggetto nella $AvailabilitySet locale.</span><span class="sxs-lookup"><span data-stu-id="cdc42-134">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="cdc42-135">Il quarto comando crea un oggetto macchina virtuale e quindi lo archivia nella $VirtualMachine variabile.</span><span class="sxs-lookup"><span data-stu-id="cdc42-135">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="cdc42-136">Il comando assegna un nome e le dimensioni alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cdc42-136">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="cdc42-137">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="cdc42-137">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="cdc42-138">I quattro comandi seguenti assegnano valori alle variabili da usare nel comando seguente.</span><span class="sxs-lookup"><span data-stu-id="cdc42-138">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="cdc42-139">Queste stringhe possono essere specificate direttamente nel comando **Set-AzVMOperatingSystem,** quindi questo approccio viene usato solo per la leggibilità.</span><span class="sxs-lookup"><span data-stu-id="cdc42-139">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="cdc42-140">Tuttavia, è possibile usare un approccio come questo negli script.</span><span class="sxs-lookup"><span data-stu-id="cdc42-140">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="cdc42-141">Il comando finale imposta le proprietà del sistema operativo per la macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="cdc42-141">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="cdc42-142">Il comando usa le credenziali archiviate in $Credential.</span><span class="sxs-lookup"><span data-stu-id="cdc42-142">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="cdc42-143">Per alcuni parametri il comando usa le variabili assegnate nei comandi precedenti.</span><span class="sxs-lookup"><span data-stu-id="cdc42-143">The command uses variables assigned in previous commands for some parameters.</span></span>
<span data-ttu-id="cdc42-144">Il comando abilita l'accesso a scelta rapida nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cdc42-144">The command enables Hotpatching on the virtual machine.</span></span>

### <span data-ttu-id="cdc42-145">Esempio 3: Impostare le proprietà del sistema operativo per una nuova macchina virtuale Linux</span><span class="sxs-lookup"><span data-stu-id="cdc42-145">Example 3: Set operating system properties for a new Linux virtual machine</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="cdc42-146">Il primo comando converte una password in una stringa sicura e quindi la archivia nella $SecurePassword variabile.</span><span class="sxs-lookup"><span data-stu-id="cdc42-146">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="cdc42-147">Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="cdc42-147">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="cdc42-148">Il secondo comando crea le credenziali per l'utente FullerP e la password archiviate in $SecurePassword, quindi archivia le credenziali nella variabile $Credential utente.</span><span class="sxs-lookup"><span data-stu-id="cdc42-148">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="cdc42-149">Per altre informazioni, digitare `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="cdc42-149">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="cdc42-150">Il terzo comando ottiene il set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia l'oggetto nella $AvailabilitySet locale.</span><span class="sxs-lookup"><span data-stu-id="cdc42-150">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="cdc42-151">Il quarto comando crea un oggetto macchina virtuale e quindi lo archivia nella $VirtualMachine variabile.</span><span class="sxs-lookup"><span data-stu-id="cdc42-151">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="cdc42-152">Il comando assegna un nome e le dimensioni alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cdc42-152">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="cdc42-153">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="cdc42-153">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="cdc42-154">I due comandi seguenti assegnano valori alle variabili da usare nel comando seguente.</span><span class="sxs-lookup"><span data-stu-id="cdc42-154">The next two commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="cdc42-155">Il comando finale imposta le proprietà del sistema operativo per la macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="cdc42-155">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="cdc42-156">Il comando usa le credenziali archiviate in $Credential.</span><span class="sxs-lookup"><span data-stu-id="cdc42-156">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="cdc42-157">Per alcuni parametri il comando usa le variabili assegnate nei comandi precedenti.</span><span class="sxs-lookup"><span data-stu-id="cdc42-157">The command uses variables assigned in previous commands for some parameters.</span></span>
<span data-ttu-id="cdc42-158">Il comando imposta il valore della modalità patch nella macchina virtuale su "AutomaticByPlatform".</span><span class="sxs-lookup"><span data-stu-id="cdc42-158">The command sets the patch mode value on the virtual machine to "AutomaticByPlatform".</span></span>

## <span data-ttu-id="cdc42-159">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdc42-159">PARAMETERS</span></span>

### <span data-ttu-id="cdc42-160">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="cdc42-160">-ComputerName</span></span>
<span data-ttu-id="cdc42-161">Specifica il nome del computer.</span><span class="sxs-lookup"><span data-stu-id="cdc42-161">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="cdc42-162">-Credential</span><span class="sxs-lookup"><span data-stu-id="cdc42-162">-Credential</span></span>
<span data-ttu-id="cdc42-163">Specifica il nome utente e la password della macchina virtuale come **oggetto PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="cdc42-163">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="cdc42-164">Per ottenere le credenziali, usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="cdc42-164">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="cdc42-165">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="cdc42-165">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="cdc42-166">-CustomData</span><span class="sxs-lookup"><span data-stu-id="cdc42-166">-CustomData</span></span>
<span data-ttu-id="cdc42-167">Specifica una stringa da passare alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cdc42-167">Specifies a string to be passed to the virtual machine.</span></span> <span data-ttu-id="cdc42-168">Per altre informazioni, vedere [Dati personalizzati nelle macchine virtuali di Azure.](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data)</span><span class="sxs-lookup"><span data-stu-id="cdc42-168">For more information see [Custom Data on Azure VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data).</span></span>
<span data-ttu-id="cdc42-169">**Nota: non è consigliabile archiviare informazioni riservate in dati personalizzati.**</span><span class="sxs-lookup"><span data-stu-id="cdc42-169">**Note: It is not recommended to store sensitive information in custom data.**</span></span>


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

### <span data-ttu-id="cdc42-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc42-170">-DefaultProfile</span></span>
<span data-ttu-id="cdc42-171">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cdc42-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdc42-172">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="cdc42-172">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="cdc42-173">Indica che questo cmdlet disabilita l'autenticazione tramite password.</span><span class="sxs-lookup"><span data-stu-id="cdc42-173">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="cdc42-174">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="cdc42-174">-DisableVMAgent</span></span>
<span data-ttu-id="cdc42-175">Disabilitare provisioning agente VM.</span><span class="sxs-lookup"><span data-stu-id="cdc42-175">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="cdc42-176">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="cdc42-176">-EnableAutoUpdate</span></span>
<span data-ttu-id="cdc42-177">Indica che questo cmdlet abilita l'aggiornamento automatico.</span><span class="sxs-lookup"><span data-stu-id="cdc42-177">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="cdc42-178">-EnableHotpatching</span><span class="sxs-lookup"><span data-stu-id="cdc42-178">-EnableHotpatching</span></span>
<span data-ttu-id="cdc42-179">Consente ai clienti di applicare patch alle macchine virtuali Azure senza dover riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="cdc42-179">Enables customers to patch their Azure VMs without requiring a reboot.</span></span> <span data-ttu-id="cdc42-180">Per enableHotpatching, "provisionVMAgent" deve essere impostato su true e "patchMode" deve essere impostato su "AutomaticByPlatform".</span><span class="sxs-lookup"><span data-stu-id="cdc42-180">For enableHotpatching, the 'provisionVMAgent' must be set to true and 'patchMode' must be set to 'AutomaticByPlatform'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc42-181">-Linux</span><span class="sxs-lookup"><span data-stu-id="cdc42-181">-Linux</span></span>
<span data-ttu-id="cdc42-182">Indica che il tipo di sistema operativo è Linux.</span><span class="sxs-lookup"><span data-stu-id="cdc42-182">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="cdc42-183">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="cdc42-183">-PatchMode</span></span>
<span data-ttu-id="cdc42-184">Specifica la modalità di distribuzione delle patch in-guest alla macchina virtuale IaaS.</span><span class="sxs-lookup"><span data-stu-id="cdc42-184">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="cdc42-185">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="cdc42-185">Possible values are:</span></span><br>
<span data-ttu-id="cdc42-186">**Manuale:** è possibile controllare l'applicazione delle patch a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cdc42-186">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="cdc42-187">A questo scopo, applicare manualmente le patch all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cdc42-187">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="cdc42-188">In questa modalità gli aggiornamenti automatici sono disabilitati; la proprietà WindowsConfiguration.enableAutomaticUpdates deve essere false</span><span class="sxs-lookup"><span data-stu-id="cdc42-188">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="cdc42-189">**AutomaticByOS:** la macchina virtuale verrà aggiornata automaticamente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cdc42-189">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="cdc42-190">La proprietà WindowsConfiguration.enableAutomaticUpdates deve essere true.</span><span class="sxs-lookup"><span data-stu-id="cdc42-190">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="cdc42-191">**AutomaticByPlatform:** la macchina virtuale verrà aggiornata automaticamente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cdc42-191">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="cdc42-192">Le proprietà provisionVMAgent e WindowsConfiguration.enableAutomaticUpdates devono essere true</span><span class="sxs-lookup"><span data-stu-id="cdc42-192">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc42-193">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="cdc42-193">-ProvisionVMAgent</span></span>
<span data-ttu-id="cdc42-194">Indica che le impostazioni richiedono l'installazione dell'agente della macchina virtuale nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cdc42-194">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="cdc42-195">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="cdc42-195">-TimeZone</span></span>
<span data-ttu-id="cdc42-196">Specifica il fuso orario della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cdc42-196">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="cdc42-197">ad esempio Ora \" solare \" Pacifico.</span><span class="sxs-lookup"><span data-stu-id="cdc42-197">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="cdc42-198">I valori possibili possono essere [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) da fusi orari restituiti da [TimeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="cdc42-198">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="cdc42-199">-VM</span><span class="sxs-lookup"><span data-stu-id="cdc42-199">-VM</span></span>
<span data-ttu-id="cdc42-200">Specifica l'oggetto della macchina virtuale locale su cui impostare le proprietà del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cdc42-200">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="cdc42-201">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cdc42-201">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="cdc42-202">Creare un oggetto macchina virtuale usando il cmdlet New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="cdc42-202">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="cdc42-203">-Windows</span><span class="sxs-lookup"><span data-stu-id="cdc42-203">-Windows</span></span>
<span data-ttu-id="cdc42-204">Indica che il tipo di sistema operativo è Windows.</span><span class="sxs-lookup"><span data-stu-id="cdc42-204">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="cdc42-205">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="cdc42-205">-WinRMCertificateUrl</span></span>
<span data-ttu-id="cdc42-206">Specifica l'URI di un certificato WinRM.</span><span class="sxs-lookup"><span data-stu-id="cdc42-206">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="cdc42-207">Questa cartella deve essere archiviata in un Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="cdc42-207">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="cdc42-208">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="cdc42-208">-WinRMHttp</span></span>
<span data-ttu-id="cdc42-209">Indica che il sistema operativo usa HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="cdc42-209">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="cdc42-210">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="cdc42-210">-WinRMHttps</span></span>
<span data-ttu-id="cdc42-211">Indica che questo sistema operativo usa HTTPS WinRM.</span><span class="sxs-lookup"><span data-stu-id="cdc42-211">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="cdc42-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc42-212">CommonParameters</span></span>
<span data-ttu-id="cdc42-213">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdc42-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc42-214">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cdc42-214">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc42-215">INPUT</span><span class="sxs-lookup"><span data-stu-id="cdc42-215">INPUTS</span></span>

### <span data-ttu-id="cdc42-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cdc42-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="cdc42-217">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cdc42-217">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="cdc42-218">System.String</span><span class="sxs-lookup"><span data-stu-id="cdc42-218">System.String</span></span>

### <span data-ttu-id="cdc42-219">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="cdc42-219">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="cdc42-220">System.Uri</span><span class="sxs-lookup"><span data-stu-id="cdc42-220">System.Uri</span></span>

## <span data-ttu-id="cdc42-221">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdc42-221">OUTPUTS</span></span>

### <span data-ttu-id="cdc42-222">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cdc42-222">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="cdc42-223">NOTE</span><span class="sxs-lookup"><span data-stu-id="cdc42-223">NOTES</span></span>

## <span data-ttu-id="cdc42-224">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdc42-224">RELATED LINKS</span></span>

[<span data-ttu-id="cdc42-225">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="cdc42-225">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="cdc42-226">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="cdc42-226">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


