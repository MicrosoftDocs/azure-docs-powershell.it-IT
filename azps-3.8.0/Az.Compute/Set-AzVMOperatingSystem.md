---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 01d1b07ec861b5eeb02d4590001e304936bde395
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022582"
---
# <span data-ttu-id="3dd40-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3dd40-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="3dd40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3dd40-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd40-103">Imposta le proprietà del sistema operativo per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3dd40-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="3dd40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dd40-104">SYNTAX</span></span>

### <span data-ttu-id="3dd40-105">Windows (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3dd40-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dd40-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="3dd40-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dd40-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="3dd40-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dd40-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="3dd40-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dd40-109">Linux</span><span class="sxs-lookup"><span data-stu-id="3dd40-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3dd40-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dd40-110">DESCRIPTION</span></span>
<span data-ttu-id="3dd40-111">Il cmdlet **set-AzVMOperatingSystem** imposta le proprietà del sistema operativo per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3dd40-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="3dd40-112">È possibile specificare le credenziali di accesso, il nome del computer e il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3dd40-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="3dd40-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dd40-113">EXAMPLES</span></span>

### <span data-ttu-id="3dd40-114">Esempio 1: impostare le proprietà del sistema operativo per una nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="3dd40-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="3dd40-115">Il primo comando converte una password in una stringa sicura e la archivia nella variabile $SecurePassword.</span><span class="sxs-lookup"><span data-stu-id="3dd40-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="3dd40-116">Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="3dd40-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="3dd40-117">Il secondo comando crea una credenziale per l'utente FullerP e la password archiviata in $SecurePassword e quindi archivia le credenziali nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="3dd40-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="3dd40-118">Per altre informazioni, digitare `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="3dd40-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="3dd40-119">Il terzo comando ottiene il set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="3dd40-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="3dd40-120">Il quarto comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="3dd40-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="3dd40-121">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3dd40-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="3dd40-122">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="3dd40-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="3dd40-123">I quattro comandi successivi assegnano i valori alle variabili da usare con il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="3dd40-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="3dd40-124">Poiché puoi specificare queste stringhe direttamente nel comando **set-AzVMOperatingSystem** , questo approccio viene usato solo per la leggibilità.</span><span class="sxs-lookup"><span data-stu-id="3dd40-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="3dd40-125">Tuttavia, è possibile usare un approccio come questo negli script.</span><span class="sxs-lookup"><span data-stu-id="3dd40-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="3dd40-126">Il comando Final imposta le proprietà del sistema operativo per la macchina virtuale archiviate in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="3dd40-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="3dd40-127">Il comando usa le credenziali archiviate in $Credential.</span><span class="sxs-lookup"><span data-stu-id="3dd40-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="3dd40-128">Il comando usa le variabili assegnate nei comandi precedenti per alcuni parametri.</span><span class="sxs-lookup"><span data-stu-id="3dd40-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="3dd40-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3dd40-129">PARAMETERS</span></span>

### <span data-ttu-id="3dd40-130">-Nomecomputer</span><span class="sxs-lookup"><span data-stu-id="3dd40-130">-ComputerName</span></span>
<span data-ttu-id="3dd40-131">Specifica il nome del computer.</span><span class="sxs-lookup"><span data-stu-id="3dd40-131">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="3dd40-132">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="3dd40-132">-Credential</span></span>
<span data-ttu-id="3dd40-133">Specifica il nome utente e la password per la macchina virtuale come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="3dd40-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="3dd40-134">Per ottenere una credenziale, usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="3dd40-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="3dd40-135">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="3dd40-135">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="3dd40-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="3dd40-136">-CustomData</span></span>
<span data-ttu-id="3dd40-137">Specifica una stringa codificata di base-64 di dati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="3dd40-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="3dd40-138">Questa operazione viene decodificata in una matrice binaria che viene salvata come file nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3dd40-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="3dd40-139">La lunghezza massima della matrice binaria è di 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="3dd40-139">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="3dd40-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd40-140">-DefaultProfile</span></span>
<span data-ttu-id="3dd40-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3dd40-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dd40-142">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="3dd40-142">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="3dd40-143">Indica che questo cmdlet disabilita l'autenticazione tramite password.</span><span class="sxs-lookup"><span data-stu-id="3dd40-143">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="3dd40-144">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="3dd40-144">-DisableVMAgent</span></span>
<span data-ttu-id="3dd40-145">Disabilitare il provisioning di un agente VM.</span><span class="sxs-lookup"><span data-stu-id="3dd40-145">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="3dd40-146">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="3dd40-146">-EnableAutoUpdate</span></span>
<span data-ttu-id="3dd40-147">Indica che questo cmdlet Abilita l'aggiornamento automatico.</span><span class="sxs-lookup"><span data-stu-id="3dd40-147">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="3dd40-148">-Linux</span><span class="sxs-lookup"><span data-stu-id="3dd40-148">-Linux</span></span>
<span data-ttu-id="3dd40-149">Indica che il tipo di sistema operativo è Linux.</span><span class="sxs-lookup"><span data-stu-id="3dd40-149">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="3dd40-150">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="3dd40-150">-ProvisionVMAgent</span></span>
<span data-ttu-id="3dd40-151">Indica che le impostazioni richiedono l'installazione dell'agente macchina virtuale nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3dd40-151">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="3dd40-152">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="3dd40-152">-TimeZone</span></span>
<span data-ttu-id="3dd40-153">Specifica il fuso orario per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3dd40-153">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="3dd40-154">-VM</span><span class="sxs-lookup"><span data-stu-id="3dd40-154">-VM</span></span>
<span data-ttu-id="3dd40-155">Specifica l'oggetto macchina virtuale locale in cui impostare le proprietà del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3dd40-155">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="3dd40-156">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="3dd40-156">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="3dd40-157">Creare un oggetto macchina virtuale usando il cmdlet New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="3dd40-157">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="3dd40-158">-Windows</span><span class="sxs-lookup"><span data-stu-id="3dd40-158">-Windows</span></span>
<span data-ttu-id="3dd40-159">Indica che il tipo di sistema operativo è Windows.</span><span class="sxs-lookup"><span data-stu-id="3dd40-159">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="3dd40-160">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="3dd40-160">-WinRMCertificateUrl</span></span>
<span data-ttu-id="3dd40-161">Specifica l'URI di un certificato WinRM.</span><span class="sxs-lookup"><span data-stu-id="3dd40-161">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="3dd40-162">Questa operazione deve essere archiviata in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="3dd40-162">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="3dd40-163">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="3dd40-163">-WinRMHttp</span></span>
<span data-ttu-id="3dd40-164">Indica che questo sistema operativo Usa HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="3dd40-164">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="3dd40-165">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="3dd40-165">-WinRMHttps</span></span>
<span data-ttu-id="3dd40-166">Indica che questo sistema operativo usa HTTPS WinRM.</span><span class="sxs-lookup"><span data-stu-id="3dd40-166">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="3dd40-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd40-167">CommonParameters</span></span>
<span data-ttu-id="3dd40-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dd40-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd40-169">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dd40-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd40-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3dd40-170">INPUTS</span></span>

### <span data-ttu-id="3dd40-171">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3dd40-171">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="3dd40-172">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3dd40-172">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3dd40-173">System. String</span><span class="sxs-lookup"><span data-stu-id="3dd40-173">System.String</span></span>

### <span data-ttu-id="3dd40-174">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="3dd40-174">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="3dd40-175">System. Uri</span><span class="sxs-lookup"><span data-stu-id="3dd40-175">System.Uri</span></span>

## <span data-ttu-id="3dd40-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dd40-176">OUTPUTS</span></span>

### <span data-ttu-id="3dd40-177">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3dd40-177">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="3dd40-178">Note</span><span class="sxs-lookup"><span data-stu-id="3dd40-178">NOTES</span></span>

## <span data-ttu-id="3dd40-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dd40-179">RELATED LINKS</span></span>

[<span data-ttu-id="3dd40-180">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="3dd40-180">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="3dd40-181">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="3dd40-181">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


