---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: b2e7264b5c0f54f18e295a86f9abb1cbd51dc4b8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861278"
---
# <span data-ttu-id="99992-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="99992-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="99992-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99992-102">SYNOPSIS</span></span>
<span data-ttu-id="99992-103">Rimuove un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="99992-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="99992-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99992-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99992-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99992-105">DESCRIPTION</span></span>
<span data-ttu-id="99992-106">Il cmdlet **Remove-AzKeyVaultCertificate** rimuove un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="99992-106">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="99992-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99992-107">EXAMPLES</span></span>

### <span data-ttu-id="99992-108">Esempio 1: rimuovere un certificato</span><span class="sxs-lookup"><span data-stu-id="99992-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="99992-109">Questo comando rimuove il certificato denominato SelfSigned01 dal Vault chiave denominato ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="99992-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="99992-110">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="99992-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="99992-111">Di conseguenza, il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="99992-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="99992-112">Esempio 3: eliminare definitivamente il certificato eliminato dal caveau della chiave</span><span class="sxs-lookup"><span data-stu-id="99992-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="99992-113">Questo comando rimuove definitivamente il certificato denominato "CERT" dall'archivio della chiave denominato "contoso".</span><span class="sxs-lookup"><span data-stu-id="99992-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="99992-114">L'esecuzione di questo cmdlet richiede l'autorizzazione "Purge", che deve essere stata concessa in precedenza e esplicitamente all'utente in questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="99992-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="99992-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99992-115">PARAMETERS</span></span>

### <span data-ttu-id="99992-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99992-116">-DefaultProfile</span></span>
<span data-ttu-id="99992-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="99992-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99992-118">-Force</span><span class="sxs-lookup"><span data-stu-id="99992-118">-Force</span></span>
<span data-ttu-id="99992-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="99992-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99992-120">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="99992-120">-InRemovedState</span></span>
<span data-ttu-id="99992-121">Se presente, rimuove definitivamente il certificato eliminato in precedenza</span><span class="sxs-lookup"><span data-stu-id="99992-121">If present, removes the previously deleted certificate permanently</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99992-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="99992-122">-Name</span></span>
<span data-ttu-id="99992-123">Specifica il nome del certificato rimosso da questo cmdlet da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="99992-123">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="99992-124">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un certificato basato sul nome specificato da questo parametro, il nome del Vault della chiave e l'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="99992-124">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99992-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99992-125">-PassThru</span></span>
<span data-ttu-id="99992-126">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="99992-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="99992-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="99992-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99992-128">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="99992-128">-VaultName</span></span>
<span data-ttu-id="99992-129">Specifica il nome del Vault chiave da cui questo cmdlet rimuove un certificato.</span><span class="sxs-lookup"><span data-stu-id="99992-129">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="99992-130">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="99992-130">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99992-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99992-131">-Confirm</span></span>
<span data-ttu-id="99992-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99992-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99992-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99992-133">-WhatIf</span></span>
<span data-ttu-id="99992-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99992-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99992-135">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99992-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99992-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99992-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99992-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99992-137">CommonParameters</span></span>
<span data-ttu-id="99992-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99992-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99992-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99992-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99992-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99992-140">INPUTS</span></span>

### <span data-ttu-id="99992-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="99992-141">None</span></span>
<span data-ttu-id="99992-142">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="99992-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="99992-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99992-143">OUTPUTS</span></span>

### <span data-ttu-id="99992-144">Microsoft. Azure. Commands. Vault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="99992-144">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="99992-145">Note</span><span class="sxs-lookup"><span data-stu-id="99992-145">NOTES</span></span>

## <span data-ttu-id="99992-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99992-146">RELATED LINKS</span></span>

[<span data-ttu-id="99992-147">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="99992-147">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="99992-148">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="99992-148">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="99992-149">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="99992-149">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="99992-150">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="99992-150">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
