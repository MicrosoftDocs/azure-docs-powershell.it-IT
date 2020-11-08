---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
ms.openlocfilehash: 298d6bac6b2c1b37cff47a22a1647caafdb3e843
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202511"
---
# <span data-ttu-id="3c83b-101">Restore-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3c83b-101">Restore-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="3c83b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c83b-102">SYNOPSIS</span></span>
<span data-ttu-id="3c83b-103">Ripristina un certificato in un Vault chiave da un file di backup.</span><span class="sxs-lookup"><span data-stu-id="3c83b-103">Restores a certificate in a key vault from a backup file.</span></span>

## <span data-ttu-id="3c83b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c83b-104">SYNTAX</span></span>

### <span data-ttu-id="3c83b-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c83b-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c83b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3c83b-106">ByInputObject</span></span>
```
Restore-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c83b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3c83b-107">ByResourceId</span></span>
```
Restore-AzKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c83b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c83b-108">DESCRIPTION</span></span>
<span data-ttu-id="3c83b-109">Il cmdlet **Restore-AzKeyVaultCertificate** crea un certificato nell'archivio chiavi specificato da un file di backup.</span><span class="sxs-lookup"><span data-stu-id="3c83b-109">The **Restore-AzKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="3c83b-110">Questo certificato è una replica del certificato di cui è stato eseguito il backup nel file di input e ha lo stesso nome del certificato originale.</span><span class="sxs-lookup"><span data-stu-id="3c83b-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="3c83b-111">Se il Vault della chiave contiene già un certificato con lo stesso nome, il cmdlet non riesce invece di sovrascrivere il certificato originale.</span><span class="sxs-lookup"><span data-stu-id="3c83b-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="3c83b-112">Se il backup contiene più versioni di un certificato, tutte le versioni verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="3c83b-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="3c83b-113">Il Vault chiave in cui ripristinare il certificato può essere diverso da quello della chiave a cui è stato eseguito il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="3c83b-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="3c83b-114">Tuttavia, il Vault della chiave deve usare lo stesso abbonamento ed essere in un'area di Azure nella stessa geografia (ad esempio, Nord America).</span><span class="sxs-lookup"><span data-stu-id="3c83b-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="3c83b-115">Vedere il Centro protezione di Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) per il mapping delle aree di Azure alle geografie.</span><span class="sxs-lookup"><span data-stu-id="3c83b-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="3c83b-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c83b-116">EXAMPLES</span></span>

### <span data-ttu-id="3c83b-117">Esempio 1: ripristinare un certificato di backup</span><span class="sxs-lookup"><span data-stu-id="3c83b-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/25/2018 3:47:41 AM

                [Not After]
                  11/25/2018 2:57:41 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Purgeable
Enabled       : True
Expires       : 11/25/2018 10:57:41 AM
NotBefore     : 5/25/2018 10:47:41 AM
Created       : 5/25/2018 10:57:41 AM
Updated       : 5/25/2018 10:57:41 AM
Tags          : 
VaultName     : MyKeyVault
Name          : cert1
Version       : bd406f6d6b3a41a1a1c633494d8c3c3a
Id            : https://mykeyvault.vault.azure.net:443/certificates/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
```

<span data-ttu-id="3c83b-118">Questo comando ripristina un certificato, incluse tutte le relative versioni, dal file di backup denominato backup. BLOB nel caveau della chiave denominato MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="3c83b-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="3c83b-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c83b-119">PARAMETERS</span></span>

### <span data-ttu-id="3c83b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c83b-120">-DefaultProfile</span></span>
<span data-ttu-id="3c83b-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c83b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c83b-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="3c83b-122">-InputFile</span></span>
<span data-ttu-id="3c83b-123">File di input.</span><span class="sxs-lookup"><span data-stu-id="3c83b-123">Input file.</span></span>
<span data-ttu-id="3c83b-124">File di input contenente il BLOB di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="3c83b-124">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c83b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c83b-125">-InputObject</span></span>
<span data-ttu-id="3c83b-126">Oggetto Vault</span><span class="sxs-lookup"><span data-stu-id="3c83b-126">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c83b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c83b-127">-ResourceId</span></span>
<span data-ttu-id="3c83b-128">ID risorsa di un Vault</span><span class="sxs-lookup"><span data-stu-id="3c83b-128">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c83b-129">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="3c83b-129">-VaultName</span></span>
<span data-ttu-id="3c83b-130">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="3c83b-130">Vault name.</span></span>
<span data-ttu-id="3c83b-131">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="3c83b-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c83b-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3c83b-132">-Confirm</span></span>
<span data-ttu-id="3c83b-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c83b-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c83b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c83b-134">-WhatIf</span></span>
<span data-ttu-id="3c83b-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c83b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c83b-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c83b-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c83b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c83b-137">CommonParameters</span></span>
<span data-ttu-id="3c83b-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c83b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c83b-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c83b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c83b-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c83b-140">INPUTS</span></span>

### <span data-ttu-id="3c83b-141">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3c83b-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="3c83b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3c83b-142">System.String</span></span>

## <span data-ttu-id="3c83b-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c83b-143">OUTPUTS</span></span>

### <span data-ttu-id="3c83b-144">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3c83b-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="3c83b-145">Note</span><span class="sxs-lookup"><span data-stu-id="3c83b-145">NOTES</span></span>

## <span data-ttu-id="3c83b-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c83b-146">RELATED LINKS</span></span>
