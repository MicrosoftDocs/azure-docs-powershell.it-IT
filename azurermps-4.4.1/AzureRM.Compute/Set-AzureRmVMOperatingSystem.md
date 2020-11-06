---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
ms.openlocfilehash: 2d742a70f1ae95d362d5ceafcc117f1296dc2cb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521970"
---
# <span data-ttu-id="b4e0c-101">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b4e0c-101">Set-AzureRmVMOperatingSystem</span></span>

## <span data-ttu-id="b4e0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e0c-103">Imposta le proprietà del sistema operativo per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-103">Sets operating system properties for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4e0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4e0c-104">SYNTAX</span></span>

### <span data-ttu-id="b4e0c-105">Windows (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b4e0c-105">Windows (Default)</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4e0c-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="b4e0c-106">WindowsWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4e0c-107">Linux</span><span class="sxs-lookup"><span data-stu-id="b4e0c-107">Linux</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4e0c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4e0c-108">DESCRIPTION</span></span>
<span data-ttu-id="b4e0c-109">Il cmdlet **set-AzureRmVMOperatingSystem** imposta le proprietà del sistema operativo per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-109">The **Set-AzureRmVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="b4e0c-110">È possibile specificare le credenziali di accesso, il nome del computer e il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="b4e0c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4e0c-111">EXAMPLES</span></span>

### <span data-ttu-id="b4e0c-112">Esempio 1: impostare le proprietà del sistema operativo per una nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="b4e0c-112">Example 1: Set operating system properties for a new virtual machines</span></span>
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

<span data-ttu-id="b4e0c-113">Il primo comando converte una password in una stringa sicura e la archivia nella variabile $SecurePassword.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="b4e0c-114">Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="b4e0c-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="b4e0c-115">Il secondo comando crea una credenziale per l'utente FullerP e la password archiviata in $SecurePassword e quindi archivia le credenziali nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="b4e0c-116">Per altre informazioni, digitare `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="b4e0c-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="b4e0c-117">Il terzo comando ottiene il set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="b4e0c-118">Il quarto comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b4e0c-119">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b4e0c-120">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="b4e0c-121">I quattro comandi successivi assegnano i valori alle variabili da usare con il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="b4e0c-122">Poiché puoi specificare queste stringhe direttamente nel comando **set-AzureRmVMOperatingSystem** , questo approccio viene usato solo per la leggibilità.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-122">Because you could specify these strings directly in the **Set-AzureRmVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="b4e0c-123">Tuttavia, è possibile usare un approccio come questo negli script.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="b4e0c-124">Il comando Final imposta le proprietà del sistema operativo per la macchina virtuale archiviate in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b4e0c-125">Il comando usa le credenziali archiviate in $Credential.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="b4e0c-126">Il comando usa le variabili assegnate nei comandi precedenti per alcuni parametri.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="b4e0c-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4e0c-127">PARAMETERS</span></span>

### <span data-ttu-id="b4e0c-128">-Nomecomputer</span><span class="sxs-lookup"><span data-stu-id="b4e0c-128">-ComputerName</span></span>
<span data-ttu-id="b4e0c-129">Specifica il nome del computer.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-129">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="b4e0c-130">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="b4e0c-130">-Credential</span></span>
<span data-ttu-id="b4e0c-131">Specifica il nome utente e la password per la macchina virtuale come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="b4e0c-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="b4e0c-132">Per ottenere una credenziale, usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="b4e0c-133">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="b4e0c-133">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="b4e0c-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="b4e0c-134">-CustomData</span></span>
<span data-ttu-id="b4e0c-135">Specifica una stringa codificata di base-64 di dati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="b4e0c-136">Questa operazione viene decodificata in una matrice binaria che viene salvata come file nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="b4e0c-137">La lunghezza massima della matrice binaria è di 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-137">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="b4e0c-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e0c-138">-DefaultProfile</span></span>
<span data-ttu-id="b4e0c-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e0c-140">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="b4e0c-140">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="b4e0c-141">Indica che questo cmdlet disabilita l'autenticazione tramite password.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-141">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="b4e0c-142">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="b4e0c-142">-EnableAutoUpdate</span></span>
<span data-ttu-id="b4e0c-143">Indica che questo cmdlet Abilita l'aggiornamento automatico.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-143">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e0c-144">-Linux</span><span class="sxs-lookup"><span data-stu-id="b4e0c-144">-Linux</span></span>
<span data-ttu-id="b4e0c-145">Indica che il tipo di sistema operativo è Linux.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-145">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="b4e0c-146">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="b4e0c-146">-ProvisionVMAgent</span></span>
<span data-ttu-id="b4e0c-147">Indica che le impostazioni richiedono l'installazione dell'agente macchina virtuale nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-147">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="b4e0c-148">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="b4e0c-148">-TimeZone</span></span>
<span data-ttu-id="b4e0c-149">Specifica il fuso orario per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-149">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e0c-150">-VM</span><span class="sxs-lookup"><span data-stu-id="b4e0c-150">-VM</span></span>
<span data-ttu-id="b4e0c-151">Specifica l'oggetto macchina virtuale locale in cui impostare le proprietà del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-151">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="b4e0c-152">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-152">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="b4e0c-153">Creare un oggetto macchina virtuale usando il cmdlet New-AzureRmVMConfig.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-153">Create a virtual machine object by using the New-AzureRmVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="b4e0c-154">-Windows</span><span class="sxs-lookup"><span data-stu-id="b4e0c-154">-Windows</span></span>
<span data-ttu-id="b4e0c-155">Indica che il tipo di sistema operativo è Windows.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-155">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e0c-156">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="b4e0c-156">-WinRMCertificateUrl</span></span>
<span data-ttu-id="b4e0c-157">Specifica l'URI di un certificato WinRM.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-157">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="b4e0c-158">Questa operazione deve essere archiviata in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-158">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e0c-159">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="b4e0c-159">-WinRMHttp</span></span>
<span data-ttu-id="b4e0c-160">Indica che questo sistema operativo Usa HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-160">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e0c-161">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="b4e0c-161">-WinRMHttps</span></span>
<span data-ttu-id="b4e0c-162">Indica che questo sistema operativo usa HTTPS WinRM.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-162">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e0c-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e0c-163">CommonParameters</span></span>
<span data-ttu-id="b4e0c-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4e0c-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e0c-165">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4e0c-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e0c-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4e0c-166">INPUTS</span></span>

## <span data-ttu-id="b4e0c-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4e0c-167">OUTPUTS</span></span>

## <span data-ttu-id="b4e0c-168">Note</span><span class="sxs-lookup"><span data-stu-id="b4e0c-168">NOTES</span></span>

## <span data-ttu-id="b4e0c-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4e0c-169">RELATED LINKS</span></span>

[<span data-ttu-id="b4e0c-170">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b4e0c-170">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="b4e0c-171">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="b4e0c-171">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


