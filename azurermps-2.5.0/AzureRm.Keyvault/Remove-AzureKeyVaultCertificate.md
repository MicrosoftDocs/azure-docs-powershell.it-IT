---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: 662304cff991da0d9ffe9d946e63bc94ba51e4a9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865805"
---
# <span data-ttu-id="ce1e7-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ce1e7-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="ce1e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce1e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ce1e7-103">Rimuove un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce1e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce1e7-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce1e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce1e7-105">DESCRIPTION</span></span>
<span data-ttu-id="ce1e7-106">Il cmdlet **Remove-AzureKeyVaultCertificate** rimuove un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-106">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="ce1e7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce1e7-107">EXAMPLES</span></span>

### <span data-ttu-id="ce1e7-108">Esempio 1: rimuovere un certificato</span><span class="sxs-lookup"><span data-stu-id="ce1e7-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="ce1e7-109">Questo comando rimuove il certificato denominato SelfSigned01 dal Vault chiave denominato ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="ce1e7-110">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="ce1e7-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ce1e7-111">Di conseguenza, il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="ce1e7-112">Esempio 3: eliminare definitivamente il certificato eliminato dal caveau della chiave</span><span class="sxs-lookup"><span data-stu-id="ce1e7-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="ce1e7-113">Questo comando rimuove definitivamente il certificato denominato "CERT" dall'archivio della chiave denominato "contoso".</span><span class="sxs-lookup"><span data-stu-id="ce1e7-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="ce1e7-114">L'esecuzione di questo cmdlet richiede l'autorizzazione "Purge", che deve essere stata concessa in precedenza e esplicitamente all'utente in questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="ce1e7-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce1e7-115">PARAMETERS</span></span>

### <span data-ttu-id="ce1e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce1e7-116">-DefaultProfile</span></span>
<span data-ttu-id="ce1e7-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ce1e7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce1e7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ce1e7-118">-Force</span></span>
<span data-ttu-id="ce1e7-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ce1e7-120">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="ce1e7-120">-InRemovedState</span></span>
<span data-ttu-id="ce1e7-121">Se presente, rimuove definitivamente il certificato eliminato in precedenza</span><span class="sxs-lookup"><span data-stu-id="ce1e7-121">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="ce1e7-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce1e7-122">-Name</span></span>
<span data-ttu-id="ce1e7-123">Specifica il nome del certificato rimosso da questo cmdlet da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-123">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="ce1e7-124">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un certificato basato sul nome specificato da questo parametro, il nome del Vault della chiave e l'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-124">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="ce1e7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce1e7-125">-PassThru</span></span>
<span data-ttu-id="ce1e7-126">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ce1e7-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ce1e7-128">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="ce1e7-128">-VaultName</span></span>
<span data-ttu-id="ce1e7-129">Specifica il nome del Vault chiave da cui questo cmdlet rimuove un certificato.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-129">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="ce1e7-130">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-130">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="ce1e7-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ce1e7-131">-Confirm</span></span>
<span data-ttu-id="ce1e7-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce1e7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce1e7-133">-WhatIf</span></span>
<span data-ttu-id="ce1e7-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce1e7-135">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce1e7-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce1e7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce1e7-137">CommonParameters</span></span>
<span data-ttu-id="ce1e7-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce1e7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce1e7-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce1e7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce1e7-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce1e7-140">INPUTS</span></span>

## <span data-ttu-id="ce1e7-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce1e7-141">OUTPUTS</span></span>

### <span data-ttu-id="ce1e7-142">Microsoft. Azure. Commands. Vault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="ce1e7-142">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="ce1e7-143">Note</span><span class="sxs-lookup"><span data-stu-id="ce1e7-143">NOTES</span></span>

## <span data-ttu-id="ce1e7-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce1e7-144">RELATED LINKS</span></span>

[<span data-ttu-id="ce1e7-145">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ce1e7-145">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="ce1e7-146">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ce1e7-146">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="ce1e7-147">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ce1e7-147">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="ce1e7-148">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="ce1e7-148">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
