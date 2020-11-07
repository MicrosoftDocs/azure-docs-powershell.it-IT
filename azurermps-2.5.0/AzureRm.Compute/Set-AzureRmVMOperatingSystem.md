---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmoperatingsystem
schema: 2.0.0
ms.openlocfilehash: 0eea5d3a4f379b61e5d66e04b66e7812abaf75f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866893"
---
# <span data-ttu-id="f69a1-101">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="f69a1-101">Set-AzureRmVMOperatingSystem</span></span>

## <span data-ttu-id="f69a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f69a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f69a1-103">Imposta le proprietà del sistema operativo per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f69a1-103">Sets operating system properties for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f69a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f69a1-104">SYNTAX</span></span>

### <span data-ttu-id="f69a1-105">Windows (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f69a1-105">Windows (Default)</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f69a1-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="f69a1-106">WindowsWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f69a1-107">Linux</span><span class="sxs-lookup"><span data-stu-id="f69a1-107">Linux</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f69a1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f69a1-108">DESCRIPTION</span></span>
<span data-ttu-id="f69a1-109">Il cmdlet **set-AzureRmVMOperatingSystem** imposta le proprietà del sistema operativo per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f69a1-109">The **Set-AzureRmVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="f69a1-110">È possibile specificare le credenziali di accesso, il nome del computer e il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f69a1-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="f69a1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f69a1-111">EXAMPLES</span></span>

### <span data-ttu-id="f69a1-112">Esempio 1: impostare le proprietà del sistema operativo per una nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="f69a1-112">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="f69a1-113">Il primo comando converte una password in una stringa sicura e la archivia nella variabile $SecurePassword.</span><span class="sxs-lookup"><span data-stu-id="f69a1-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="f69a1-114">Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="f69a1-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="f69a1-115">Il secondo comando crea una credenziale per l'utente FullerP e la password archiviata in $SecurePassword e quindi archivia le credenziali nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="f69a1-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="f69a1-116">Per altre informazioni, digitare `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="f69a1-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="f69a1-117">Il terzo comando ottiene il set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="f69a1-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="f69a1-118">Il quarto comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f69a1-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="f69a1-119">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f69a1-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="f69a1-120">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="f69a1-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="f69a1-121">I quattro comandi successivi assegnano i valori alle variabili da usare con il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="f69a1-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="f69a1-122">Poiché puoi specificare queste stringhe direttamente nel comando **set-AzureRmVMOperatingSystem** , questo approccio viene usato solo per la leggibilità.</span><span class="sxs-lookup"><span data-stu-id="f69a1-122">Because you could specify these strings directly in the **Set-AzureRmVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="f69a1-123">Tuttavia, è possibile usare un approccio come questo negli script.</span><span class="sxs-lookup"><span data-stu-id="f69a1-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="f69a1-124">Il comando Final imposta le proprietà del sistema operativo per la macchina virtuale archiviate in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f69a1-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="f69a1-125">Il comando usa le credenziali archiviate in $Credential.</span><span class="sxs-lookup"><span data-stu-id="f69a1-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="f69a1-126">Il comando usa le variabili assegnate nei comandi precedenti per alcuni parametri.</span><span class="sxs-lookup"><span data-stu-id="f69a1-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="f69a1-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f69a1-127">PARAMETERS</span></span>

### <span data-ttu-id="f69a1-128">-Nomecomputer</span><span class="sxs-lookup"><span data-stu-id="f69a1-128">-ComputerName</span></span>
<span data-ttu-id="f69a1-129">Specifica il nome del computer.</span><span class="sxs-lookup"><span data-stu-id="f69a1-129">Specifies the name of the computer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69a1-130">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="f69a1-130">-Credential</span></span>
<span data-ttu-id="f69a1-131">Specifica il nome utente e la password per la macchina virtuale come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="f69a1-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="f69a1-132">Per ottenere una credenziale, usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="f69a1-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="f69a1-133">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="f69a1-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69a1-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="f69a1-134">-CustomData</span></span>
<span data-ttu-id="f69a1-135">Specifica una stringa codificata di base-64 di dati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="f69a1-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="f69a1-136">Questa operazione viene decodificata in una matrice binaria che viene salvata come file nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f69a1-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="f69a1-137">La lunghezza massima della matrice binaria è di 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="f69a1-137">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="f69a1-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f69a1-138">-DefaultProfile</span></span>
<span data-ttu-id="f69a1-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f69a1-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f69a1-140">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="f69a1-140">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="f69a1-141">Indica che questo cmdlet disabilita l'autenticazione tramite password.</span><span class="sxs-lookup"><span data-stu-id="f69a1-141">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69a1-142">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="f69a1-142">-EnableAutoUpdate</span></span>
<span data-ttu-id="f69a1-143">Indica che questo cmdlet Abilita l'aggiornamento automatico.</span><span class="sxs-lookup"><span data-stu-id="f69a1-143">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69a1-144">-Linux</span><span class="sxs-lookup"><span data-stu-id="f69a1-144">-Linux</span></span>
<span data-ttu-id="f69a1-145">Indica che il tipo di sistema operativo è Linux.</span><span class="sxs-lookup"><span data-stu-id="f69a1-145">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69a1-146">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="f69a1-146">-ProvisionVMAgent</span></span>
<span data-ttu-id="f69a1-147">Indica che le impostazioni richiedono l'installazione dell'agente macchina virtuale nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f69a1-147">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69a1-148">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="f69a1-148">-TimeZone</span></span>
<span data-ttu-id="f69a1-149">Specifica il fuso orario per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f69a1-149">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69a1-150">-VM</span><span class="sxs-lookup"><span data-stu-id="f69a1-150">-VM</span></span>
<span data-ttu-id="f69a1-151">Specifica l'oggetto macchina virtuale locale in cui impostare le proprietà del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f69a1-151">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="f69a1-152">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="f69a1-152">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="f69a1-153">Creare un oggetto macchina virtuale usando il cmdlet New-AzureRmVMConfig.</span><span class="sxs-lookup"><span data-stu-id="f69a1-153">Create a virtual machine object by using the New-AzureRmVMConfig cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f69a1-154">-Windows</span><span class="sxs-lookup"><span data-stu-id="f69a1-154">-Windows</span></span>
<span data-ttu-id="f69a1-155">Indica che il tipo di sistema operativo è Windows.</span><span class="sxs-lookup"><span data-stu-id="f69a1-155">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69a1-156">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="f69a1-156">-WinRMCertificateUrl</span></span>
<span data-ttu-id="f69a1-157">Specifica l'URI di un certificato WinRM.</span><span class="sxs-lookup"><span data-stu-id="f69a1-157">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="f69a1-158">Questa operazione deve essere archiviata in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="f69a1-158">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: Uri
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69a1-159">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="f69a1-159">-WinRMHttp</span></span>
<span data-ttu-id="f69a1-160">Indica che questo sistema operativo Usa HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="f69a1-160">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69a1-161">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="f69a1-161">-WinRMHttps</span></span>
<span data-ttu-id="f69a1-162">Indica che questo sistema operativo usa HTTPS WinRM.</span><span class="sxs-lookup"><span data-stu-id="f69a1-162">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69a1-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f69a1-163">CommonParameters</span></span>
<span data-ttu-id="f69a1-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f69a1-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f69a1-165">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f69a1-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f69a1-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f69a1-166">INPUTS</span></span>

### <span data-ttu-id="f69a1-167">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f69a1-167">PSVirtualMachine</span></span>
<span data-ttu-id="f69a1-168">Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f69a1-168">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="f69a1-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f69a1-169">OUTPUTS</span></span>

### <span data-ttu-id="f69a1-170">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f69a1-170">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f69a1-171">Note</span><span class="sxs-lookup"><span data-stu-id="f69a1-171">NOTES</span></span>

## <span data-ttu-id="f69a1-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f69a1-172">RELATED LINKS</span></span>

[<span data-ttu-id="f69a1-173">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f69a1-173">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="f69a1-174">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="f69a1-174">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


