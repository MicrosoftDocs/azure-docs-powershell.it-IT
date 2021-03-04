---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 3a85b92b930ef24e4cb613de28f6a66b530222cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952589"
---
# <span data-ttu-id="f0bdf-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f0bdf-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="f0bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="f0bdf-103">Elimina un'autorità di certificazione da un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="f0bdf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0bdf-104">SYNTAX</span></span>

### <span data-ttu-id="f0bdf-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f0bdf-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0bdf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f0bdf-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0bdf-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f0bdf-107">DESCRIPTION</span></span>
<span data-ttu-id="f0bdf-108">Il cmdlet **Remove-AzKeyVaultCertificateIss cmdlet** elimina un'autorità di certificazione da un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="f0bdf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0bdf-109">EXAMPLES</span></span>

### <span data-ttu-id="f0bdf-110">Esempio 1: Rimuovere un'autorità di certificazione</span><span class="sxs-lookup"><span data-stu-id="f0bdf-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="f0bdf-111">Questo comando rimuove l'autorità di certificazione denominata TestIssuer01 dal vault della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="f0bdf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0bdf-112">PARAMETERS</span></span>

### <span data-ttu-id="f0bdf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0bdf-113">-DefaultProfile</span></span>
<span data-ttu-id="f0bdf-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f0bdf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0bdf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f0bdf-115">-Force</span></span>
<span data-ttu-id="f0bdf-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f0bdf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0bdf-117">-InputObject</span></span>
<span data-ttu-id="f0bdf-118">Oggetto Certificate Issuer</span><span class="sxs-lookup"><span data-stu-id="f0bdf-118">Certificate Issuer Object</span></span>

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

### <span data-ttu-id="f0bdf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f0bdf-119">-Name</span></span>
<span data-ttu-id="f0bdf-120">Specifica il nome dell'autorità emittente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-120">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="f0bdf-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0bdf-121">-PassThru</span></span>
<span data-ttu-id="f0bdf-122">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f0bdf-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f0bdf-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f0bdf-124">-VaultName</span></span>
<span data-ttu-id="f0bdf-125">Specifica il nome di un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="f0bdf-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0bdf-126">-Confirm</span></span>
<span data-ttu-id="f0bdf-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0bdf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0bdf-128">-WhatIf</span></span>
<span data-ttu-id="f0bdf-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0bdf-130">Il cmdlet non viene eseguito. Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0bdf-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0bdf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0bdf-132">CommonParameters</span></span>
<span data-ttu-id="f0bdf-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0bdf-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0bdf-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="f0bdf-135">INPUTS</span></span>

### <span data-ttu-id="f0bdf-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f0bdf-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="f0bdf-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0bdf-137">OUTPUTS</span></span>

### <span data-ttu-id="f0bdf-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f0bdf-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="f0bdf-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="f0bdf-139">NOTES</span></span>

## <span data-ttu-id="f0bdf-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0bdf-140">RELATED LINKS</span></span>

[<span data-ttu-id="f0bdf-141">Get-AzKeyVaultCertificateIsssburg</span><span class="sxs-lookup"><span data-stu-id="f0bdf-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="f0bdf-142">Set-AzKeyVaultCertificateIsssburg</span><span class="sxs-lookup"><span data-stu-id="f0bdf-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


