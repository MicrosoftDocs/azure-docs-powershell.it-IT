---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 9a33d4efdd82ad03b94ea9a7e862fb5e13eb30d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521622"
---
# <span data-ttu-id="21765-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="21765-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="21765-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21765-102">SYNOPSIS</span></span>
<span data-ttu-id="21765-103">Rimuove un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="21765-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21765-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21765-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21765-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21765-105">DESCRIPTION</span></span>
<span data-ttu-id="21765-106">Il cmdlet **Remove-AzureKeyVaultCertificate** rimuove un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="21765-106">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="21765-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21765-107">EXAMPLES</span></span>

### <span data-ttu-id="21765-108">Esempio 1: rimuovere un certificato</span><span class="sxs-lookup"><span data-stu-id="21765-108">Example 1: Remove a certificate</span></span>
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

<span data-ttu-id="21765-109">Questo comando rimuove il certificato denominato SelfSigned01 dal Vault chiave denominato ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="21765-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="21765-110">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="21765-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="21765-111">Di conseguenza, il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="21765-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="21765-112">Esempio 3: eliminare definitivamente il certificato eliminato dal caveau della chiave</span><span class="sxs-lookup"><span data-stu-id="21765-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="21765-113">Questo comando rimuove definitivamente il certificato denominato "CERT" dall'archivio della chiave denominato "contoso".</span><span class="sxs-lookup"><span data-stu-id="21765-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="21765-114">L'esecuzione di questo cmdlet richiede l'autorizzazione "Purge", che deve essere stata concessa in precedenza e esplicitamente all'utente in questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="21765-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="21765-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21765-115">PARAMETERS</span></span>

### <span data-ttu-id="21765-116">-Force</span><span class="sxs-lookup"><span data-stu-id="21765-116">-Force</span></span>
<span data-ttu-id="21765-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="21765-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="21765-118">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="21765-118">-InRemovedState</span></span>
<span data-ttu-id="21765-119">Se presente, rimuove definitivamente il certificato eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="21765-119">If present, removes the previously deleted certificate permanently.</span></span>

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

### <span data-ttu-id="21765-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="21765-120">-Name</span></span>
<span data-ttu-id="21765-121">Specifica il nome del certificato rimosso da questo cmdlet da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="21765-121">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="21765-122">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un certificato basato sul nome specificato da questo parametro, il nome del Vault della chiave e l'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="21765-122">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="21765-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21765-123">-PassThru</span></span>
<span data-ttu-id="21765-124">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="21765-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="21765-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="21765-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="21765-126">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="21765-126">-VaultName</span></span>
<span data-ttu-id="21765-127">Specifica il nome del Vault chiave da cui questo cmdlet rimuove un certificato.</span><span class="sxs-lookup"><span data-stu-id="21765-127">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="21765-128">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="21765-128">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21765-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="21765-129">-Confirm</span></span>
<span data-ttu-id="21765-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21765-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21765-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21765-131">-WhatIf</span></span>
<span data-ttu-id="21765-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21765-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21765-133">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21765-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21765-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21765-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21765-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21765-135">-DefaultProfile</span></span>
<span data-ttu-id="21765-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21765-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21765-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21765-137">CommonParameters</span></span>
<span data-ttu-id="21765-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21765-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21765-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21765-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21765-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21765-140">INPUTS</span></span>

## <span data-ttu-id="21765-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21765-141">OUTPUTS</span></span>

### <span data-ttu-id="21765-142">Microsoft. Azure. Commands. Vault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="21765-142">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="21765-143">Note</span><span class="sxs-lookup"><span data-stu-id="21765-143">NOTES</span></span>

## <span data-ttu-id="21765-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21765-144">RELATED LINKS</span></span>

[<span data-ttu-id="21765-145">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="21765-145">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="21765-146">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="21765-146">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="21765-147">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="21765-147">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="21765-148">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="21765-148">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
