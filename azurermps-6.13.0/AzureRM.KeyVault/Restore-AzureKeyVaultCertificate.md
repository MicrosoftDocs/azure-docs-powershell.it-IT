---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7955ecd02d40ac3dff891b8eb315a39ccf985ebb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688114"
---
# <span data-ttu-id="280e9-101">Restore-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="280e9-101">Restore-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="280e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="280e9-102">SYNOPSIS</span></span>
<span data-ttu-id="280e9-103">Ripristina un certificato in un Vault chiave da un file di backup.</span><span class="sxs-lookup"><span data-stu-id="280e9-103">Restores a certificate in a key vault from a backup file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="280e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="280e9-104">SYNTAX</span></span>

### <span data-ttu-id="280e9-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="280e9-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="280e9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="280e9-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="280e9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="280e9-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="280e9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="280e9-108">DESCRIPTION</span></span>
<span data-ttu-id="280e9-109">Il cmdlet **Restore-AzureKeyVaultCertificate** crea un certificato nell'archivio chiavi specificato da un file di backup.</span><span class="sxs-lookup"><span data-stu-id="280e9-109">The **Restore-AzureKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="280e9-110">Questo certificato è una replica del certificato di cui è stato eseguito il backup nel file di input e ha lo stesso nome del certificato originale.</span><span class="sxs-lookup"><span data-stu-id="280e9-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="280e9-111">Se il Vault della chiave contiene già un certificato con lo stesso nome, il cmdlet non riesce invece di sovrascrivere il certificato originale.</span><span class="sxs-lookup"><span data-stu-id="280e9-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="280e9-112">Se il backup contiene più versioni di un certificato, tutte le versioni verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="280e9-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="280e9-113">Il Vault chiave in cui ripristinare il certificato può essere diverso da quello della chiave a cui è stato eseguito il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="280e9-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="280e9-114">Tuttavia, il Vault della chiave deve usare lo stesso abbonamento ed essere in un'area di Azure nella stessa geografia (ad esempio, Nord America).</span><span class="sxs-lookup"><span data-stu-id="280e9-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="280e9-115">Vedere il Centro protezione di Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) per il mapping delle aree di Azure alle geografie.</span><span class="sxs-lookup"><span data-stu-id="280e9-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="280e9-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="280e9-116">EXAMPLES</span></span>

### <span data-ttu-id="280e9-117">Esempio 1: ripristinare un certificato di backup</span><span class="sxs-lookup"><span data-stu-id="280e9-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="280e9-118">Questo comando ripristina un certificato, incluse tutte le relative versioni, dal file di backup denominato backup. BLOB nel caveau della chiave denominato MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="280e9-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="280e9-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="280e9-119">PARAMETERS</span></span>

### <span data-ttu-id="280e9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="280e9-120">-DefaultProfile</span></span>
<span data-ttu-id="280e9-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="280e9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="280e9-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="280e9-122">-InputFile</span></span>
<span data-ttu-id="280e9-123">File di input.</span><span class="sxs-lookup"><span data-stu-id="280e9-123">Input file.</span></span>
<span data-ttu-id="280e9-124">File di input contenente il BLOB di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="280e9-124">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="280e9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="280e9-125">-InputObject</span></span>
<span data-ttu-id="280e9-126">Oggetto Vault</span><span class="sxs-lookup"><span data-stu-id="280e9-126">KeyVault object</span></span>

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

### <span data-ttu-id="280e9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="280e9-127">-ResourceId</span></span>
<span data-ttu-id="280e9-128">ID risorsa di un Vault</span><span class="sxs-lookup"><span data-stu-id="280e9-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="280e9-129">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="280e9-129">-VaultName</span></span>
<span data-ttu-id="280e9-130">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="280e9-130">Vault name.</span></span>
<span data-ttu-id="280e9-131">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="280e9-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="280e9-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="280e9-132">-Confirm</span></span>
<span data-ttu-id="280e9-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="280e9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="280e9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="280e9-134">-WhatIf</span></span>
<span data-ttu-id="280e9-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="280e9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="280e9-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="280e9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="280e9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="280e9-137">CommonParameters</span></span>
<span data-ttu-id="280e9-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="280e9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="280e9-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="280e9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="280e9-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="280e9-140">INPUTS</span></span>

### <span data-ttu-id="280e9-141">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="280e9-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="280e9-142">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="280e9-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="280e9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="280e9-143">System.String</span></span>

## <span data-ttu-id="280e9-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="280e9-144">OUTPUTS</span></span>

### <span data-ttu-id="280e9-145">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="280e9-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="280e9-146">Note</span><span class="sxs-lookup"><span data-stu-id="280e9-146">NOTES</span></span>

## <span data-ttu-id="280e9-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="280e9-147">RELATED LINKS</span></span>