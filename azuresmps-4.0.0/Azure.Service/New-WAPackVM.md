---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030860"
---
# <span data-ttu-id="3bfba-101">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3bfba-101">New-WAPackVM</span></span>

## <span data-ttu-id="3bfba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3bfba-102">SYNOPSIS</span></span>
<span data-ttu-id="3bfba-103">Crea una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3bfba-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="3bfba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3bfba-104">SYNTAX</span></span>

### <span data-ttu-id="3bfba-105">CreateVMFromTemplate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3bfba-105">CreateVMFromTemplate (Default)</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3bfba-106">CreateLinuxVMFromTemplate</span><span class="sxs-lookup"><span data-stu-id="3bfba-106">CreateLinuxVMFromTemplate</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3bfba-107">CreateVMFromOSDisk</span><span class="sxs-lookup"><span data-stu-id="3bfba-107">CreateVMFromOSDisk</span></span>
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3bfba-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bfba-108">DESCRIPTION</span></span>
<span data-ttu-id="3bfba-109">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="3bfba-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="3bfba-110">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3bfba-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3bfba-111">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3bfba-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3bfba-112">Il cmdlet **New-WAPackVM** crea una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3bfba-112">The **New-WAPackVM** cmdlet creates a virtual machine.</span></span>

## <span data-ttu-id="3bfba-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3bfba-113">EXAMPLES</span></span>

### <span data-ttu-id="3bfba-114">Esempio 1: creare una macchina virtuale per il sistema operativo Windows usando un modello</span><span class="sxs-lookup"><span data-stu-id="3bfba-114">Example 1: Create a virtual machine for the Windows operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

<span data-ttu-id="3bfba-115">Il primo comando crea un oggetto **PSCredential** e lo archivia nella variabile $Credentials.</span><span class="sxs-lookup"><span data-stu-id="3bfba-115">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="3bfba-116">Il cmdlet richiede l'accesso a un account e una password.</span><span class="sxs-lookup"><span data-stu-id="3bfba-116">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="3bfba-117">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="3bfba-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="3bfba-118">Il secondo comando ottiene il modello di macchina virtuale denominato ContosoTemplate04 usando il cmdlet **Get-WAPackVMTemplate** e lo archivia nella variabile $template.</span><span class="sxs-lookup"><span data-stu-id="3bfba-118">The second command gets the virtual machine template named ContosoTemplate04 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="3bfba-119">Il comando finale crea una macchina virtuale denominata ContosoV023, in base al modello archiviato nella variabile $Template.</span><span class="sxs-lookup"><span data-stu-id="3bfba-119">The final command creates a virtual machine named ContosoV023, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="3bfba-120">Il comando specifica il parametro *Windows* e, di conseguenza, la macchina virtuale deve eseguire una versione del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="3bfba-120">The command specifies the *Windows* parameter, and, therefore, the virtual machine must run a version of the Windows operating system.</span></span>

### <span data-ttu-id="3bfba-121">Esempio 2: creare una macchina virtuale per il sistema operativo Linux usando un modello</span><span class="sxs-lookup"><span data-stu-id="3bfba-121">Example 2: Create a virtual machine for the Linux operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

<span data-ttu-id="3bfba-122">Il primo comando crea un oggetto **PSCredential** e lo archivia nella variabile $Credentials.</span><span class="sxs-lookup"><span data-stu-id="3bfba-122">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>

<span data-ttu-id="3bfba-123">Il secondo comando ottiene il modello di macchina virtuale denominato ContosoTemplate19 usando il cmdlet **Get-WAPackVMTemplate** e lo archivia nella variabile $template.</span><span class="sxs-lookup"><span data-stu-id="3bfba-123">The second command gets the virtual machine template named ContosoTemplate19 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="3bfba-124">Il comando finale crea una macchina virtuale denominata ContosoV028, in base al modello archiviato nella variabile $Template.</span><span class="sxs-lookup"><span data-stu-id="3bfba-124">The final command creates a virtual machine named ContosoV028, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="3bfba-125">Il comando specifica il parametro *Linux* e, di conseguenza, la macchina virtuale deve eseguire una versione del sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="3bfba-125">The command specifies the *Linux* parameter, and, therefore, the virtual machine must run a version of the Linux operating system.</span></span>

### <span data-ttu-id="3bfba-126">Esempio 3: creare una macchina virtuale da un profilo disco e dimensioni del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3bfba-126">Example 3: Create a virtual machine from an operating system disk and size profile</span></span>
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

<span data-ttu-id="3bfba-127">Il primo comando ottiene un disco del sistema operativo denominato ContosoDiskOS usando il cmdlet **Get-WAPackVMOSDisk** e lo archivia nella variabile $OSDisk.</span><span class="sxs-lookup"><span data-stu-id="3bfba-127">The first command gets an operating system disk named ContosoDiskOS by using the **Get-WAPackVMOSDisk** cmdlet, and then stores it in the $OSDisk variable.</span></span>

<span data-ttu-id="3bfba-128">Il secondo comando ottiene il profilo di dimensione denominato MediumSizeVM usando il cmdlet **Get-WAPackVMSizeProfile** e lo archivia nella variabile $SizeProfile.</span><span class="sxs-lookup"><span data-stu-id="3bfba-128">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores it in the $SizeProfile variable.</span></span>

<span data-ttu-id="3bfba-129">Il comando finale crea una macchina virtuale denominata ContosoV073 dal disco del sistema operativo archiviato in $OSDisk e il profilo delle dimensioni archiviato in $SizeProfile.</span><span class="sxs-lookup"><span data-stu-id="3bfba-129">The final command creates a virtual machine named ContosoV073 from the operating system disk stored in $OSDisk and the size profile stored in $SizeProfile.</span></span>

## <span data-ttu-id="3bfba-130">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3bfba-130">PARAMETERS</span></span>

### <span data-ttu-id="3bfba-131">-AdministratorSSHKey</span><span class="sxs-lookup"><span data-stu-id="3bfba-131">-AdministratorSSHKey</span></span>
<span data-ttu-id="3bfba-132">Specifica la chiave Secure Shell (SSH) per l'account Administrator.</span><span class="sxs-lookup"><span data-stu-id="3bfba-132">Specifies the Secure Shell (SSH) key for the Administrator account.</span></span>

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bfba-133">-Linux</span><span class="sxs-lookup"><span data-stu-id="3bfba-133">-Linux</span></span>
<span data-ttu-id="3bfba-134">Indica che il cmdlet crea una macchina virtuale per l'esecuzione del sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="3bfba-134">Indicates that the cmdlet creates a virtual machine to run the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bfba-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="3bfba-135">-Name</span></span>
<span data-ttu-id="3bfba-136">Specifica un nome per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3bfba-136">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="3bfba-137">-OSDisk</span><span class="sxs-lookup"><span data-stu-id="3bfba-137">-OSDisk</span></span>
<span data-ttu-id="3bfba-138">Specifica un disco del sistema operativo come oggetto **VirtualHardDisk** .</span><span class="sxs-lookup"><span data-stu-id="3bfba-138">Specifies an operating system disk as a **VirtualHardDisk** object.</span></span>
<span data-ttu-id="3bfba-139">Per ottenere un disco del sistema operativo, usare il cmdlet **Get-WAPackVMOSDisk** .</span><span class="sxs-lookup"><span data-stu-id="3bfba-139">To obtain an operating system disk, use the **Get-WAPackVMOSDisk** cmdlet.</span></span>

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bfba-140">-ProductKey</span><span class="sxs-lookup"><span data-stu-id="3bfba-140">-ProductKey</span></span>
<span data-ttu-id="3bfba-141">Specifica un codice Product Key.</span><span class="sxs-lookup"><span data-stu-id="3bfba-141">Specifies a product key.</span></span>
<span data-ttu-id="3bfba-142">Il codice Product Key è un numero di 25 cifre che identifica la licenza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="3bfba-142">The product key is a 25 digit number that identifies the product license.</span></span>
<span data-ttu-id="3bfba-143">Usare un codice Product Key per un sistema operativo che si prevede di installare in una macchina virtuale o in un host.</span><span class="sxs-lookup"><span data-stu-id="3bfba-143">Use a product key for an operating system that you plan to install on a virtual machine or host.</span></span>

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bfba-144">-Profile</span><span class="sxs-lookup"><span data-stu-id="3bfba-144">-Profile</span></span>
<span data-ttu-id="3bfba-145">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bfba-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3bfba-146">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3bfba-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3bfba-147">-Modello</span><span class="sxs-lookup"><span data-stu-id="3bfba-147">-Template</span></span>
<span data-ttu-id="3bfba-148">Specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="3bfba-148">Specifies a template.</span></span>
<span data-ttu-id="3bfba-149">Il cmdlet crea una macchina virtuale in base al modello specificato.</span><span class="sxs-lookup"><span data-stu-id="3bfba-149">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="3bfba-150">Per ottenere un oggetto modello, usare il cmdlet Get-WAPackVMTemplate.</span><span class="sxs-lookup"><span data-stu-id="3bfba-150">To obtain a template object, use the Get-WAPackVMTemplate cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bfba-151">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="3bfba-151">-VMCredential</span></span>
<span data-ttu-id="3bfba-152">Specifica le credenziali per l'account di amministratore locale.</span><span class="sxs-lookup"><span data-stu-id="3bfba-152">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="3bfba-153">Per ottenere un oggetto **PSCredential** , usare il cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="3bfba-153">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="3bfba-154">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="3bfba-154">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bfba-155">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="3bfba-155">-VMSizeProfile</span></span>
<span data-ttu-id="3bfba-156">Specifica un profilo di dimensione per una macchina virtuale come oggetto **HardwareProfile** .</span><span class="sxs-lookup"><span data-stu-id="3bfba-156">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="3bfba-157">Per ottenere un profilo di dimensione, usare il cmdlet **Get-WAPackVMSizeProfile** .</span><span class="sxs-lookup"><span data-stu-id="3bfba-157">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bfba-158">-VNet</span><span class="sxs-lookup"><span data-stu-id="3bfba-158">-VNet</span></span>
<span data-ttu-id="3bfba-159">Specifica una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3bfba-159">Specifies a virtual network.</span></span>
<span data-ttu-id="3bfba-160">Il cmdlet connette la macchina virtuale alla rete virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="3bfba-160">The cmdlet connects the virtual machine to the virtual network that you specify.</span></span>
<span data-ttu-id="3bfba-161">Per ottenere una rete virtuale, usare il cmdlet **Get-WAPackVNet** .</span><span class="sxs-lookup"><span data-stu-id="3bfba-161">To obtain a virtual network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bfba-162">-Windows</span><span class="sxs-lookup"><span data-stu-id="3bfba-162">-Windows</span></span>
<span data-ttu-id="3bfba-163">Indica che il cmdlet crea una macchina virtuale per l'esecuzione del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="3bfba-163">Indicates that the cmdlet creates a virtual machine to run the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bfba-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bfba-164">CommonParameters</span></span>
<span data-ttu-id="3bfba-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bfba-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bfba-166">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bfba-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bfba-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3bfba-167">INPUTS</span></span>

## <span data-ttu-id="3bfba-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3bfba-168">OUTPUTS</span></span>

## <span data-ttu-id="3bfba-169">Note</span><span class="sxs-lookup"><span data-stu-id="3bfba-169">NOTES</span></span>

## <span data-ttu-id="3bfba-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3bfba-170">RELATED LINKS</span></span>

[<span data-ttu-id="3bfba-171">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3bfba-171">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="3bfba-172">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3bfba-172">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="3bfba-173">Riavviare-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3bfba-173">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="3bfba-174">Curriculum vitae-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3bfba-174">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="3bfba-175">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3bfba-175">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="3bfba-176">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3bfba-176">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="3bfba-177">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3bfba-177">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="3bfba-178">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3bfba-178">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="3bfba-179">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="3bfba-179">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)

[<span data-ttu-id="3bfba-180">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="3bfba-180">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)

[<span data-ttu-id="3bfba-181">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="3bfba-181">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


