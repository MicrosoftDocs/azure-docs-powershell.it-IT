---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: 70d6d39ed3e2083bf0f52e9e56808b7d36f1cc24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514287"
---
# <span data-ttu-id="adde4-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="adde4-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="adde4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="adde4-102">SYNOPSIS</span></span>
<span data-ttu-id="adde4-103">Elimina un'operazione di certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="adde4-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adde4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="adde4-104">SYNTAX</span></span>

### <span data-ttu-id="adde4-105">Predefinita</span><span class="sxs-lookup"><span data-stu-id="adde4-105">Default</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adde4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="adde4-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adde4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adde4-107">DESCRIPTION</span></span>
<span data-ttu-id="adde4-108">Il cmdlet **Remove-AzureKeyVaultCertificateOperation** Elimina un'operazione di certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="adde4-108">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="adde4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="adde4-109">EXAMPLES</span></span>

### <span data-ttu-id="adde4-110">Esempio 1: rimuovere un'operazione di certificato</span><span class="sxs-lookup"><span data-stu-id="adde4-110">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="adde4-111">Questo comando rimuove l'operazione di certificato denominata TestCert01 dall'archivio della chiave ContosoKV01 senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="adde4-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="adde4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="adde4-112">PARAMETERS</span></span>

### <span data-ttu-id="adde4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adde4-113">-DefaultProfile</span></span>
<span data-ttu-id="adde4-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="adde4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adde4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="adde4-115">-Force</span></span>
<span data-ttu-id="adde4-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="adde4-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="adde4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adde4-117">-InputObject</span></span>
<span data-ttu-id="adde4-118">Oggetto Operation</span><span class="sxs-lookup"><span data-stu-id="adde4-118">Operation object</span></span>

```yaml
Type: PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adde4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="adde4-119">-Name</span></span>
<span data-ttu-id="adde4-120">Specifica il nome di un certificato.</span><span class="sxs-lookup"><span data-stu-id="adde4-120">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adde4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adde4-121">-PassThru</span></span>
<span data-ttu-id="adde4-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="adde4-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="adde4-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="adde4-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="adde4-124">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="adde4-124">-VaultName</span></span>
<span data-ttu-id="adde4-125">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="adde4-125">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adde4-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="adde4-126">-Confirm</span></span>
<span data-ttu-id="adde4-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adde4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adde4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adde4-128">-WhatIf</span></span>
<span data-ttu-id="adde4-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="adde4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adde4-130">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="adde4-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adde4-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="adde4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adde4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adde4-132">CommonParameters</span></span>
<span data-ttu-id="adde4-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adde4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adde4-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adde4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adde4-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="adde4-135">INPUTS</span></span>

### <span data-ttu-id="adde4-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="adde4-136">None</span></span>
<span data-ttu-id="adde4-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="adde4-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="adde4-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="adde4-138">OUTPUTS</span></span>

### <span data-ttu-id="adde4-139">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="adde4-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="adde4-140">Note</span><span class="sxs-lookup"><span data-stu-id="adde4-140">NOTES</span></span>

## <span data-ttu-id="adde4-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="adde4-141">RELATED LINKS</span></span>

[<span data-ttu-id="adde4-142">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="adde4-142">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="adde4-143">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="adde4-143">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

