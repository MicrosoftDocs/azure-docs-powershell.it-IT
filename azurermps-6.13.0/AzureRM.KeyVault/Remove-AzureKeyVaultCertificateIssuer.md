---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: dc49237d4722384d04228d3b8e9736411ed41bde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686180"
---
# <span data-ttu-id="f60e0-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f60e0-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="f60e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f60e0-102">SYNOPSIS</span></span>
<span data-ttu-id="f60e0-103">Elimina l'emittente di un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f60e0-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f60e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f60e0-104">SYNTAX</span></span>

### <span data-ttu-id="f60e0-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f60e0-105">Default (Default)</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f60e0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f60e0-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f60e0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f60e0-107">DESCRIPTION</span></span>
<span data-ttu-id="f60e0-108">Il cmdlet **Remove-AzureKeyVaultCertificateIssuer** Elimina un emittente di certificati da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f60e0-108">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="f60e0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f60e0-109">EXAMPLES</span></span>

### <span data-ttu-id="f60e0-110">Esempio 1: rimuovere un emittente di certificati</span><span class="sxs-lookup"><span data-stu-id="f60e0-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="f60e0-111">Questo comando rimuove l'autorità di certificazione denominata TestIssuer01 dal Vault della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="f60e0-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="f60e0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f60e0-112">PARAMETERS</span></span>

### <span data-ttu-id="f60e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f60e0-113">-DefaultProfile</span></span>
<span data-ttu-id="f60e0-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f60e0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f60e0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f60e0-115">-Force</span></span>
<span data-ttu-id="f60e0-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f60e0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f60e0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f60e0-117">-InputObject</span></span>
<span data-ttu-id="f60e0-118">Oggetto dell'autorità di certificazione</span><span class="sxs-lookup"><span data-stu-id="f60e0-118">Certificate Issuer Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f60e0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f60e0-119">-Name</span></span>
<span data-ttu-id="f60e0-120">Specifica il nome dell'emittente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f60e0-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f60e0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f60e0-121">-PassThru</span></span>
<span data-ttu-id="f60e0-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="f60e0-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f60e0-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f60e0-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f60e0-124">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="f60e0-124">-VaultName</span></span>
<span data-ttu-id="f60e0-125">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f60e0-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="f60e0-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f60e0-126">-Confirm</span></span>
<span data-ttu-id="f60e0-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f60e0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f60e0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f60e0-128">-WhatIf</span></span>
<span data-ttu-id="f60e0-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f60e0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f60e0-130">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f60e0-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f60e0-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f60e0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f60e0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f60e0-132">CommonParameters</span></span>
<span data-ttu-id="f60e0-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f60e0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f60e0-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f60e0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f60e0-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f60e0-135">INPUTS</span></span>

### <span data-ttu-id="f60e0-136">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f60e0-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>
<span data-ttu-id="f60e0-137">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f60e0-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f60e0-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f60e0-138">OUTPUTS</span></span>

### <span data-ttu-id="f60e0-139">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f60e0-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="f60e0-140">Note</span><span class="sxs-lookup"><span data-stu-id="f60e0-140">NOTES</span></span>

## <span data-ttu-id="f60e0-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f60e0-141">RELATED LINKS</span></span>

[<span data-ttu-id="f60e0-142">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f60e0-142">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="f60e0-143">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f60e0-143">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


