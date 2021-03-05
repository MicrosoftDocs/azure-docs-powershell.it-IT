---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: f1491fcf42ace90efa012778cfb5fec7faeaee07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978462"
---
# <span data-ttu-id="8a349-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8a349-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="8a349-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a349-102">SYNOPSIS</span></span>
<span data-ttu-id="8a349-103">Rimuove un certificato da un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="8a349-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="8a349-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a349-104">SYNTAX</span></span>

### <span data-ttu-id="8a349-105">ByVaultNameAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8a349-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a349-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="8a349-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a349-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8a349-107">DESCRIPTION</span></span>
<span data-ttu-id="8a349-108">Il cmdlet **Remove-AzKeyVaultCertificate** rimuove un certificato da un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="8a349-108">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="8a349-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a349-109">EXAMPLES</span></span>

### <span data-ttu-id="8a349-110">Esempio 1: Rimuovere un certificato</span><span class="sxs-lookup"><span data-stu-id="8a349-110">Example 1: Remove a certificate</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       4/11/2018 4:28:39 PM

                     [Not After]
                       10/11/2018 4:38:39 PM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contosokv01.vault.azure.net:443/keys/selfsigned01/968c3920884a435abf8faea11f565456
SecretId           : https://contosokv01.vault.azure.net:443/secrets/selfsigned01/968c3920884a435abf8faea11f565456
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Purgeable
ScheduledPurgeDate :
DeletedDate        :
Enabled            : True
Expires            : 10/11/2018 11:38:39 PM
NotBefore          : 4/11/2018 11:28:39 PM
Created            : 4/11/2018 11:38:39 PM
Updated            : 4/11/2018 11:38:39 PM
Tags               :
VaultName          : ContosoKV01
Name               : SelfSigned01
Version            : 968c3920884a435abf8faea11f565456
Id                 : https://contosokv01.vault.azure.net:443/certificates/selfsigned01/968c3920884a435abf8faea11f565456
```

<span data-ttu-id="8a349-111">Questo comando rimuove il certificato denominato SelfSigned01 dalla chiave vault denominata ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="8a349-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="8a349-112">Questo comando specifica il *parametro Force.*</span><span class="sxs-lookup"><span data-stu-id="8a349-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8a349-113">Di conseguenza, il cmdlet non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="8a349-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="8a349-114">Esempio 2: Ripulire definitivamente il certificato eliminato dal vault delle chiavi</span><span class="sxs-lookup"><span data-stu-id="8a349-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="8a349-115">Questo comando rimuove definitivamente il certificato denominato "MyCert" dalla chiave vault denominata "Contoso".</span><span class="sxs-lookup"><span data-stu-id="8a349-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="8a349-116">Per l'esecuzione di questo cmdlet è necessaria l'autorizzazione di eliminazione, che deve essere stata concessa in precedenza ed esplicitamente all'utente in questo vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="8a349-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="8a349-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a349-117">PARAMETERS</span></span>

### <span data-ttu-id="8a349-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a349-118">-DefaultProfile</span></span>
<span data-ttu-id="8a349-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8a349-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a349-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8a349-120">-Force</span></span>
<span data-ttu-id="8a349-121">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="8a349-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8a349-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a349-122">-InputObject</span></span>
<span data-ttu-id="8a349-123">Oggetto certificato.</span><span class="sxs-lookup"><span data-stu-id="8a349-123">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a349-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="8a349-124">-InRemovedState</span></span>
<span data-ttu-id="8a349-125">Se presente, rimuove definitivamente il certificato eliminato in precedenza</span><span class="sxs-lookup"><span data-stu-id="8a349-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="8a349-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8a349-126">-Name</span></span>
<span data-ttu-id="8a349-127">Specifica il nome del certificato che questo cmdlet rimuove da un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="8a349-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="8a349-128">Questo cmdlet crea il nome di dominio completo (FQDN) di un certificato in base al nome specificato da questo parametro, al nome del vault delle chiavi e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="8a349-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a349-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a349-129">-PassThru</span></span>
<span data-ttu-id="8a349-130">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="8a349-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8a349-131">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="8a349-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8a349-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8a349-132">-VaultName</span></span>
<span data-ttu-id="8a349-133">Specifica il nome del vault della chiave da cui questo cmdlet rimuove un certificato.</span><span class="sxs-lookup"><span data-stu-id="8a349-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="8a349-134">Questo cmdlet crea l'FQDN di un vault delle chiavi in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="8a349-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a349-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a349-135">-Confirm</span></span>
<span data-ttu-id="8a349-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a349-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a349-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a349-137">-WhatIf</span></span>
<span data-ttu-id="8a349-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a349-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a349-139">Il cmdlet non viene eseguito. Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a349-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a349-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a349-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a349-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a349-141">CommonParameters</span></span>
<span data-ttu-id="8a349-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a349-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a349-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8a349-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a349-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="8a349-144">INPUTS</span></span>

### <span data-ttu-id="8a349-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8a349-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="8a349-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a349-146">OUTPUTS</span></span>

### <span data-ttu-id="8a349-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8a349-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="8a349-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="8a349-148">NOTES</span></span>

## <span data-ttu-id="8a349-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a349-149">RELATED LINKS</span></span>

[<span data-ttu-id="8a349-150">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8a349-150">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="8a349-151">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8a349-151">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="8a349-152">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8a349-152">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="8a349-153">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="8a349-153">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
