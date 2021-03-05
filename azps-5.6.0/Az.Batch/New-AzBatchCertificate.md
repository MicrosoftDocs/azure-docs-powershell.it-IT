---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: 4ef75210204cddc8de2aa129f0997cb4f12269b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972205"
---
# <span data-ttu-id="c4599-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="c4599-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="c4599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4599-102">SYNOPSIS</span></span>
<span data-ttu-id="c4599-103">Aggiunge un certificato all'account batch specificato.</span><span class="sxs-lookup"><span data-stu-id="c4599-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="c4599-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4599-104">SYNTAX</span></span>

### <span data-ttu-id="c4599-105">File (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4599-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4599-106">RawData</span><span class="sxs-lookup"><span data-stu-id="c4599-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4599-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c4599-107">DESCRIPTION</span></span>
<span data-ttu-id="c4599-108">Il cmdlet **New-AzBatchCertificate** aggiunge un certificato all'account batch di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="c4599-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="c4599-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4599-109">EXAMPLES</span></span>

### <span data-ttu-id="c4599-110">Esempio 1: Aggiungere un certificato da un file</span><span class="sxs-lookup"><span data-stu-id="c4599-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="c4599-111">Questo comando aggiunge un certificato all'account batch specificato usando il file E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="c4599-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="c4599-112">Esempio 2: Aggiungere un certificato dai dati non elaborati</span><span class="sxs-lookup"><span data-stu-id="c4599-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="c4599-113">Il primo comando legge i dati dal file denominato MyCert.pfx nella $RawData variabile.</span><span class="sxs-lookup"><span data-stu-id="c4599-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="c4599-114">Il secondo comando aggiunge un certificato all'account batch specificato usando i dati non elaborati archiviati in $RawData.</span><span class="sxs-lookup"><span data-stu-id="c4599-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="c4599-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4599-115">PARAMETERS</span></span>

### <span data-ttu-id="c4599-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c4599-116">-BatchContext</span></span>
<span data-ttu-id="c4599-117">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c4599-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c4599-118">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c4599-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c4599-119">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="c4599-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c4599-120">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="c4599-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c4599-121">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c4599-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4599-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4599-122">-DefaultProfile</span></span>
<span data-ttu-id="c4599-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4599-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4599-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="c4599-124">-FilePath</span></span>
<span data-ttu-id="c4599-125">Specifica il percorso del file di certificato.</span><span class="sxs-lookup"><span data-stu-id="c4599-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="c4599-126">Il file del certificato deve essere in formato .cer o .pfx.</span><span class="sxs-lookup"><span data-stu-id="c4599-126">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4599-127">-Kind</span><span class="sxs-lookup"><span data-stu-id="c4599-127">-Kind</span></span>
<span data-ttu-id="c4599-128">Tipo di certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="c4599-128">The kind of certificate to create.</span></span> <span data-ttu-id="c4599-129">Se non viene specificato, si presuppone che tutti i certificati senza password siano cer e tutti i certificati con password siano PFX.</span><span class="sxs-lookup"><span data-stu-id="c4599-129">If this is not specified, it is assumed that all certificates without a password are CER and all certificates with password are PFX.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateKind
Parameter Sets: (All)
Aliases:
Accepted values: Cer, Pfx

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4599-130">-Password</span><span class="sxs-lookup"><span data-stu-id="c4599-130">-Password</span></span>
<span data-ttu-id="c4599-131">Specifica la password per accedere alla chiave privata del certificato.</span><span class="sxs-lookup"><span data-stu-id="c4599-131">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="c4599-132">È necessario specificare questo parametro se si specifica un certificato in formato PFX.</span><span class="sxs-lookup"><span data-stu-id="c4599-132">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4599-133">-RawData</span><span class="sxs-lookup"><span data-stu-id="c4599-133">-RawData</span></span>
<span data-ttu-id="c4599-134">Specifica i dati del certificato non elaborati in formato .cer o .pfx.</span><span class="sxs-lookup"><span data-stu-id="c4599-134">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: RawData
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4599-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4599-135">CommonParameters</span></span>
<span data-ttu-id="c4599-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4599-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4599-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c4599-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4599-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="c4599-138">INPUTS</span></span>

### <span data-ttu-id="c4599-139">System.Byte[]</span><span class="sxs-lookup"><span data-stu-id="c4599-139">System.Byte[]</span></span>

### <span data-ttu-id="c4599-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c4599-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c4599-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4599-141">OUTPUTS</span></span>

### <span data-ttu-id="c4599-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="c4599-142">System.Void</span></span>

## <span data-ttu-id="c4599-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="c4599-143">NOTES</span></span>

## <span data-ttu-id="c4599-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4599-144">RELATED LINKS</span></span>

[<span data-ttu-id="c4599-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="c4599-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="c4599-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c4599-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c4599-147">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="c4599-147">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="c4599-148">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="c4599-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
