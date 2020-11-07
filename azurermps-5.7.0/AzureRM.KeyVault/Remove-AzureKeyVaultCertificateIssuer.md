---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 05a59e3fd098fb32122cc85a4d39e89cf1fc66aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685986"
---
# <span data-ttu-id="3dfd1-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3dfd1-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="3dfd1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3dfd1-102">SYNOPSIS</span></span>
<span data-ttu-id="3dfd1-103">Elimina l'emittente di un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dfd1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dfd1-104">SYNTAX</span></span>

### <span data-ttu-id="3dfd1-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3dfd1-105">Default (Default)</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dfd1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3dfd1-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dfd1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dfd1-107">DESCRIPTION</span></span>
<span data-ttu-id="3dfd1-108">Il cmdlet **Remove-AzureKeyVaultCertificateIssuer** Elimina un emittente di certificati da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-108">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="3dfd1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dfd1-109">EXAMPLES</span></span>

### <span data-ttu-id="3dfd1-110">Esempio 1: rimuovere un emittente di certificati</span><span class="sxs-lookup"><span data-stu-id="3dfd1-110">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="3dfd1-111">Questo comando rimuove l'autorità di certificazione denominata TestIssuer01 dal Vault della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="3dfd1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3dfd1-112">PARAMETERS</span></span>

### <span data-ttu-id="3dfd1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dfd1-113">-DefaultProfile</span></span>
<span data-ttu-id="3dfd1-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3dfd1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3dfd1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3dfd1-115">-Force</span></span>
<span data-ttu-id="3dfd1-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3dfd1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3dfd1-117">-InputObject</span></span>
<span data-ttu-id="3dfd1-118">Oggetto dell'autorità di certificazione</span><span class="sxs-lookup"><span data-stu-id="3dfd1-118">Certificate Issuer Object</span></span>

```yaml
Type: PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfd1-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="3dfd1-119">-Name</span></span>
<span data-ttu-id="3dfd1-120">Specifica il nome dell'emittente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfd1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3dfd1-121">-PassThru</span></span>
<span data-ttu-id="3dfd1-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3dfd1-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3dfd1-124">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="3dfd1-124">-VaultName</span></span>
<span data-ttu-id="3dfd1-125">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="3dfd1-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3dfd1-126">-Confirm</span></span>
<span data-ttu-id="3dfd1-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dfd1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dfd1-128">-WhatIf</span></span>
<span data-ttu-id="3dfd1-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dfd1-130">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dfd1-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dfd1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dfd1-132">CommonParameters</span></span>
<span data-ttu-id="3dfd1-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dfd1-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dfd1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dfd1-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3dfd1-135">INPUTS</span></span>

### <span data-ttu-id="3dfd1-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3dfd1-136">None</span></span>
<span data-ttu-id="3dfd1-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3dfd1-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dfd1-138">OUTPUTS</span></span>

### <span data-ttu-id="3dfd1-139">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3dfd1-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="3dfd1-140">Note</span><span class="sxs-lookup"><span data-stu-id="3dfd1-140">NOTES</span></span>

## <span data-ttu-id="3dfd1-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dfd1-141">RELATED LINKS</span></span>

[<span data-ttu-id="3dfd1-142">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3dfd1-142">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="3dfd1-143">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3dfd1-143">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


