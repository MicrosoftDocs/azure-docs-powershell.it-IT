---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 922631712b241f6f0b516e2787a20113af8a8740
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952526"
---
# <span data-ttu-id="de7f8-101">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="de7f8-101">Remove-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="de7f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de7f8-102">SYNOPSIS</span></span>
<span data-ttu-id="de7f8-103">Elimina un'operazione di certificato da un vault chiave.</span><span class="sxs-lookup"><span data-stu-id="de7f8-103">Deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="de7f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de7f8-104">SYNTAX</span></span>

### <span data-ttu-id="de7f8-105">Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="de7f8-105">Default</span></span>
```
Remove-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de7f8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="de7f8-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de7f8-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="de7f8-107">DESCRIPTION</span></span>
<span data-ttu-id="de7f8-108">Il cmdlet **Remove-AzKeyVaultCertificateOperation** elimina un'operazione di certificato da un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="de7f8-108">The **Remove-AzKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="de7f8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de7f8-109">EXAMPLES</span></span>

### <span data-ttu-id="de7f8-110">Esempio 1: Rimuovere un'operazione di certificato</span><span class="sxs-lookup"><span data-stu-id="de7f8-110">Example 1: Remove a certificate operation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force

Id                        : https://contosokv01.vault.azure.net/certificates/testcert01/pending
Status                    : completed
StatusDetails             :
RequestId                 : f5dfd2ae486149a594dc98e800dceaaa
Target                    : https://contosokv01.vault.azure.net/certificates/testcert01
Issuer                    : Self
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
                            ==
ErrorCode                 :
ErrorMessage              :
Name                      :
VaultName                 :
```

<span data-ttu-id="de7f8-111">Questo comando rimuove l'operazione del certificato denominata TestCert01 dal vault della chiave ContosoKV01 senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="de7f8-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="de7f8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de7f8-112">PARAMETERS</span></span>

### <span data-ttu-id="de7f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de7f8-113">-DefaultProfile</span></span>
<span data-ttu-id="de7f8-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="de7f8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de7f8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="de7f8-115">-Force</span></span>
<span data-ttu-id="de7f8-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="de7f8-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de7f8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de7f8-117">-InputObject</span></span>
<span data-ttu-id="de7f8-118">Oggetto Operation</span><span class="sxs-lookup"><span data-stu-id="de7f8-118">Operation object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de7f8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="de7f8-119">-Name</span></span>
<span data-ttu-id="de7f8-120">Specifica il nome di un certificato.</span><span class="sxs-lookup"><span data-stu-id="de7f8-120">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de7f8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de7f8-121">-PassThru</span></span>
<span data-ttu-id="de7f8-122">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="de7f8-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="de7f8-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="de7f8-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de7f8-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="de7f8-124">-VaultName</span></span>
<span data-ttu-id="de7f8-125">Specifica il nome di un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="de7f8-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de7f8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de7f8-126">-Confirm</span></span>
<span data-ttu-id="de7f8-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de7f8-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de7f8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de7f8-128">-WhatIf</span></span>
<span data-ttu-id="de7f8-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de7f8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de7f8-130">Il cmdlet non viene eseguito. Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de7f8-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de7f8-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de7f8-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de7f8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de7f8-132">CommonParameters</span></span>
<span data-ttu-id="de7f8-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de7f8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de7f8-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="de7f8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de7f8-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="de7f8-135">INPUTS</span></span>

### <span data-ttu-id="de7f8-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="de7f8-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="de7f8-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de7f8-137">OUTPUTS</span></span>

### <span data-ttu-id="de7f8-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="de7f8-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="de7f8-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="de7f8-139">NOTES</span></span>

## <span data-ttu-id="de7f8-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de7f8-140">RELATED LINKS</span></span>

[<span data-ttu-id="de7f8-141">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="de7f8-141">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="de7f8-142">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="de7f8-142">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

