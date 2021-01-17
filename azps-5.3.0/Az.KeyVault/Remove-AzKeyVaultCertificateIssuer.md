---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 061b16758386cf2e279250a1ab72cdcf4180a1f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473713"
---
# <span data-ttu-id="d2532-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d2532-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="d2532-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2532-102">SYNOPSIS</span></span>
<span data-ttu-id="d2532-103">Elimina l'emittente di un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="d2532-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="d2532-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2532-104">SYNTAX</span></span>

### <span data-ttu-id="d2532-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d2532-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2532-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d2532-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2532-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2532-107">DESCRIPTION</span></span>
<span data-ttu-id="d2532-108">Il cmdlet **Remove-AzKeyVaultCertificateIssuer** Elimina un emittente di certificati da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="d2532-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="d2532-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2532-109">EXAMPLES</span></span>

### <span data-ttu-id="d2532-110">Esempio 1: rimuovere un emittente di certificati</span><span class="sxs-lookup"><span data-stu-id="d2532-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="d2532-111">Questo comando rimuove l'autorità di certificazione denominata TestIssuer01 dal Vault della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="d2532-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="d2532-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2532-112">PARAMETERS</span></span>

### <span data-ttu-id="d2532-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2532-113">-DefaultProfile</span></span>
<span data-ttu-id="d2532-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d2532-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2532-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d2532-115">-Force</span></span>
<span data-ttu-id="d2532-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d2532-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2532-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2532-117">-InputObject</span></span>
<span data-ttu-id="d2532-118">Oggetto dell'autorità di certificazione</span><span class="sxs-lookup"><span data-stu-id="d2532-118">Certificate Issuer Object</span></span>

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

### <span data-ttu-id="d2532-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2532-119">-Name</span></span>
<span data-ttu-id="d2532-120">Specifica il nome dell'emittente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d2532-120">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="d2532-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2532-121">-PassThru</span></span>
<span data-ttu-id="d2532-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="d2532-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d2532-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d2532-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d2532-124">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="d2532-124">-VaultName</span></span>
<span data-ttu-id="d2532-125">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="d2532-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="d2532-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d2532-126">-Confirm</span></span>
<span data-ttu-id="d2532-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2532-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2532-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2532-128">-WhatIf</span></span>
<span data-ttu-id="d2532-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2532-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2532-130">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2532-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2532-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2532-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2532-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2532-132">CommonParameters</span></span>
<span data-ttu-id="d2532-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2532-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2532-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2532-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2532-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2532-135">INPUTS</span></span>

### <span data-ttu-id="d2532-136">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d2532-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="d2532-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2532-137">OUTPUTS</span></span>

### <span data-ttu-id="d2532-138">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d2532-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="d2532-139">Note</span><span class="sxs-lookup"><span data-stu-id="d2532-139">NOTES</span></span>

## <span data-ttu-id="d2532-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2532-140">RELATED LINKS</span></span>

[<span data-ttu-id="d2532-141">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d2532-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="d2532-142">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d2532-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


