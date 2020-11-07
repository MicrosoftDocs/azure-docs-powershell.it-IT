---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 281b74aa14431a0bcfe0d138a78db73e28bcfeb4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863897"
---
# <span data-ttu-id="8db4f-101">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="8db4f-101">Add-AzVMSecret</span></span>

## <span data-ttu-id="8db4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8db4f-102">SYNOPSIS</span></span>
<span data-ttu-id="8db4f-103">Aggiunge un segreto a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8db4f-103">Adds a secret to a virtual machine.</span></span>

## <span data-ttu-id="8db4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8db4f-104">SYNTAX</span></span>

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8db4f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8db4f-105">DESCRIPTION</span></span>
<span data-ttu-id="8db4f-106">Il cmdlet **Add-AzVMSecret** aggiunge un segreto a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8db4f-106">The **Add-AzVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="8db4f-107">Questo valore consente di aggiungere un certificato alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8db4f-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="8db4f-108">Il segreto deve essere archiviato in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="8db4f-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="8db4f-109">Per altre informazioni su Key Vault, vedere [cos'è Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="8db4f-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="8db4f-110">Per altre informazioni sui cmdlet, vedere cmdlet di [Key Vault di Azure](https://msdn.microsoft.com/library/azure/dn868052.aspx) nella raccolta di reti Microsoft Developer o nel cmdlet [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="8db4f-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="8db4f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8db4f-111">EXAMPLES</span></span>

### <span data-ttu-id="8db4f-112">Esempio 1: aggiungere un segreto a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="8db4f-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="8db4f-113">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8db4f-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="8db4f-114">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8db4f-114">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="8db4f-115">Il secondo comando crea un oggetto Credential usando il cmdlet Get-Credential e quindi archivia il risultato nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="8db4f-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="8db4f-116">Il comando richiede un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="8db4f-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="8db4f-117">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="8db4f-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="8db4f-118">Il terzo comando usa il cmdlet **set-AzVMOperatingSystem** per configurare la macchina virtuale archiviata in $virtualmachine.</span><span class="sxs-lookup"><span data-stu-id="8db4f-118">The third command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="8db4f-119">Il quarto comando assegna un ID di archiviazione di origine alla variabile $SourceVaultId per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="8db4f-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="8db4f-120">Il comando presuppone che la variabile $SubscriptionId abbia un valore appropriato.</span><span class="sxs-lookup"><span data-stu-id="8db4f-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>

<span data-ttu-id="8db4f-121">Il quinto comando assegna un valore alla variabile $CertificateStore 01 per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="8db4f-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>

<span data-ttu-id="8db4f-122">Il sesto comando assegna un URL per un archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="8db4f-122">The sixth command assigns a URL for a certificate store.</span></span>

<span data-ttu-id="8db4f-123">Il settimo comando aggiunge un segreto alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8db4f-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="8db4f-124">Il parametro SourceVaultId specifica il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8db4f-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="8db4f-125">Il comando specifica il nome dell'archivio certificati e l'URL del certificato.</span><span class="sxs-lookup"><span data-stu-id="8db4f-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="8db4f-126">Puoi eseguire ripetutamente il **componente aggiuntivo AzVMSecret** per aggiungere segreti ad altri certificati.</span><span class="sxs-lookup"><span data-stu-id="8db4f-126">You can run the **Add-AzVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="8db4f-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8db4f-127">PARAMETERS</span></span>

### <span data-ttu-id="8db4f-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="8db4f-128">-CertificateStore</span></span>
<span data-ttu-id="8db4f-129">Specifica il nome di un archivio certificati nella macchina virtuale che esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="8db4f-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="8db4f-130">Questo cmdlet aggiunge il certificato allo Store specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8db4f-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="8db4f-131">Puoi specificare questo parametro solo per le macchine virtuali che eseguono il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="8db4f-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db4f-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="8db4f-132">-CertificateUrl</span></span>
<span data-ttu-id="8db4f-133">Specifica l'URL che punta a un segreto del Vault chiave che contiene un certificato.</span><span class="sxs-lookup"><span data-stu-id="8db4f-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>

<span data-ttu-id="8db4f-134">Il certificato è la codifica Base64 dell'oggetto JSON (JavaScript Object Notation) seguente, codificato in UTF-8:</span><span class="sxs-lookup"><span data-stu-id="8db4f-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8:</span></span>

<span data-ttu-id="8db4f-135">{"dati": " \< Codifica Base64-file \> "," DataType ":" \< File-Format \> "," password ":" \< pfx-file-password \> "}</span><span class="sxs-lookup"><span data-stu-id="8db4f-135">{ "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" }</span></span>


<span data-ttu-id="8db4f-136">Attualmente, il tipo di dati accetta solo i file PFX.</span><span class="sxs-lookup"><span data-stu-id="8db4f-136">Currently, dataType accepts only .pfx files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db4f-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8db4f-137">-DefaultProfile</span></span>
<span data-ttu-id="8db4f-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8db4f-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8db4f-139">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="8db4f-139">-SourceVaultId</span></span>
<span data-ttu-id="8db4f-140">Specifica l'ID risorsa del Vault chiave che contiene i certificati che è possibile aggiungere alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8db4f-140">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="8db4f-141">Questo valore funge anche da chiave per l'aggiunta di più certificati.</span><span class="sxs-lookup"><span data-stu-id="8db4f-141">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="8db4f-142">Questo significa che puoi usare lo stesso valore per *SourceVaultId* quando Aggiungi più certificati dallo stesso Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8db4f-142">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db4f-143">-VM</span><span class="sxs-lookup"><span data-stu-id="8db4f-143">-VM</span></span>
<span data-ttu-id="8db4f-144">Specifica l'oggetto macchina virtuale modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8db4f-144">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="8db4f-145">Per ottenere un oggetto macchina virtuale, usare il cmdlet [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="8db4f-145">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="8db4f-146">Puoi usare il cmdlet [New-AzVMConfig](./New-AzVMConfig.md) per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8db4f-146">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="8db4f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db4f-147">CommonParameters</span></span>
<span data-ttu-id="8db4f-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8db4f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db4f-149">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8db4f-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db4f-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8db4f-150">INPUTS</span></span>

### <span data-ttu-id="8db4f-151">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8db4f-151">PSVirtualMachine</span></span>
<span data-ttu-id="8db4f-152">Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8db4f-152">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="8db4f-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8db4f-153">OUTPUTS</span></span>

### <span data-ttu-id="8db4f-154">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8db4f-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="8db4f-155">Note</span><span class="sxs-lookup"><span data-stu-id="8db4f-155">NOTES</span></span>

## <span data-ttu-id="8db4f-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8db4f-156">RELATED LINKS</span></span>

[<span data-ttu-id="8db4f-157">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8db4f-157">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="8db4f-158">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="8db4f-158">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="8db4f-159">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="8db4f-159">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)
