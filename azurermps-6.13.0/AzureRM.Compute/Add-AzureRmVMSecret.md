---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMSecret.md
ms.openlocfilehash: 539c9306709b7044f2a3d7263ac8168d59f54e97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519285"
---
# <span data-ttu-id="c2b69-101">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="c2b69-101">Add-AzureRmVMSecret</span></span>

## <span data-ttu-id="c2b69-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2b69-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b69-103">Aggiunge un segreto a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c2b69-103">Adds a secret to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2b69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2b69-104">SYNTAX</span></span>

```
Add-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2b69-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2b69-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b69-106">Il cmdlet **Add-AzureRmVMSecret** aggiunge un segreto a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c2b69-106">The **Add-AzureRmVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="c2b69-107">Questo valore consente di aggiungere un certificato alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c2b69-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="c2b69-108">Il segreto deve essere archiviato in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="c2b69-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="c2b69-109">Per altre informazioni su Key Vault, vedere [cos'è Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="c2b69-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="c2b69-110">Per altre informazioni sui cmdlet, vedere cmdlet di [Key Vault di Azure](https://msdn.microsoft.com/library/azure/dn868052.aspx) nella raccolta di reti Microsoft Developer o nel cmdlet [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="c2b69-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="c2b69-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2b69-111">EXAMPLES</span></span>

### <span data-ttu-id="c2b69-112">Esempio 1: aggiungere un segreto a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="c2b69-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzureRmVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="c2b69-113">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="c2b69-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="c2b69-114">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c2b69-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="c2b69-115">Il secondo comando crea un oggetto Credential usando il cmdlet Get-Credential e quindi archivia il risultato nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="c2b69-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="c2b69-116">Il comando richiede un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="c2b69-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="c2b69-117">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="c2b69-117">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="c2b69-118">Il terzo comando usa il cmdlet **set-AzureRmVMOperatingSystem** per configurare la macchina virtuale archiviata in $virtualmachine.</span><span class="sxs-lookup"><span data-stu-id="c2b69-118">The third command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="c2b69-119">Il quarto comando assegna un ID di archiviazione di origine alla variabile $SourceVaultId per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="c2b69-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="c2b69-120">Il comando presuppone che la variabile $SubscriptionId abbia un valore appropriato.</span><span class="sxs-lookup"><span data-stu-id="c2b69-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>
<span data-ttu-id="c2b69-121">Il quinto comando assegna un valore alla variabile $CertificateStore 01 per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="c2b69-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>
<span data-ttu-id="c2b69-122">Il sesto comando assegna un URL per un archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="c2b69-122">The sixth command assigns a URL for a certificate store.</span></span>
<span data-ttu-id="c2b69-123">Il settimo comando aggiunge un segreto alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="c2b69-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="c2b69-124">Il parametro SourceVaultId specifica il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="c2b69-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="c2b69-125">Il comando specifica il nome dell'archivio certificati e l'URL del certificato.</span><span class="sxs-lookup"><span data-stu-id="c2b69-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="c2b69-126">Puoi eseguire ripetutamente il **componente aggiuntivo AzureRmVMSecret** per aggiungere segreti ad altri certificati.</span><span class="sxs-lookup"><span data-stu-id="c2b69-126">You can run the **Add-AzureRmVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="c2b69-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2b69-127">PARAMETERS</span></span>

### <span data-ttu-id="c2b69-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="c2b69-128">-CertificateStore</span></span>
<span data-ttu-id="c2b69-129">Specifica il nome di un archivio certificati nella macchina virtuale che esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="c2b69-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="c2b69-130">Questo cmdlet aggiunge il certificato allo Store specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c2b69-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="c2b69-131">Puoi specificare questo parametro solo per le macchine virtuali che eseguono il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="c2b69-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b69-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="c2b69-132">-CertificateUrl</span></span>
<span data-ttu-id="c2b69-133">Specifica l'URL che punta a un segreto del Vault chiave che contiene un certificato.</span><span class="sxs-lookup"><span data-stu-id="c2b69-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>
<span data-ttu-id="c2b69-134">Il certificato è la codifica Base64 dell'oggetto JSON (JavaScript Object Notation) seguente, codificato in UTF-8: {"data": " \<Base64-encoded-file\> ", "DataType": " \<file-format\> ", "password": " \<pfx-file-password\> "} attualmente, il tipo di dati accetta solo i file PFX.</span><span class="sxs-lookup"><span data-stu-id="c2b69-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8: { "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" } Currently, dataType accepts only .pfx files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b69-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b69-135">-DefaultProfile</span></span>
<span data-ttu-id="c2b69-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b69-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2b69-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="c2b69-137">-SourceVaultId</span></span>
<span data-ttu-id="c2b69-138">Specifica l'ID risorsa del Vault chiave che contiene i certificati che è possibile aggiungere alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c2b69-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="c2b69-139">Questo valore funge anche da chiave per l'aggiunta di più certificati.</span><span class="sxs-lookup"><span data-stu-id="c2b69-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="c2b69-140">Questo significa che puoi usare lo stesso valore per *SourceVaultId* quando Aggiungi più certificati dallo stesso Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="c2b69-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b69-141">-VM</span><span class="sxs-lookup"><span data-stu-id="c2b69-141">-VM</span></span>
<span data-ttu-id="c2b69-142">Specifica l'oggetto macchina virtuale modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2b69-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="c2b69-143">Per ottenere un oggetto macchina virtuale, usare il cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="c2b69-143">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="c2b69-144">Puoi usare il cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c2b69-144">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="c2b69-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b69-145">CommonParameters</span></span>
<span data-ttu-id="c2b69-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b69-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b69-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2b69-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b69-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2b69-148">INPUTS</span></span>

### <span data-ttu-id="c2b69-149">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c2b69-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="c2b69-150">System. String</span><span class="sxs-lookup"><span data-stu-id="c2b69-150">System.String</span></span>

## <span data-ttu-id="c2b69-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2b69-151">OUTPUTS</span></span>

### <span data-ttu-id="c2b69-152">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c2b69-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c2b69-153">Note</span><span class="sxs-lookup"><span data-stu-id="c2b69-153">NOTES</span></span>

## <span data-ttu-id="c2b69-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2b69-154">RELATED LINKS</span></span>

[<span data-ttu-id="c2b69-155">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c2b69-155">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="c2b69-156">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="c2b69-156">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="c2b69-157">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c2b69-157">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)