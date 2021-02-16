---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 4d3be232e97f71a030548fd0b3754a7472b80b22
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185510"
---
# <span data-ttu-id="32347-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="32347-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="32347-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32347-102">SYNOPSIS</span></span>
<span data-ttu-id="32347-103">Imposta un'autorità di certificazione in un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="32347-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="32347-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32347-104">SYNTAX</span></span>

### <span data-ttu-id="32347-105">Espanso (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="32347-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32347-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="32347-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32347-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="32347-107">DESCRIPTION</span></span>
<span data-ttu-id="32347-108">Il Set-AzKeyVaultCertificateIssuer cmdlet imposta un'autorità di certificazione in un vault chiave.</span><span class="sxs-lookup"><span data-stu-id="32347-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="32347-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32347-109">EXAMPLES</span></span>

### <span data-ttu-id="32347-110">Esempio 1: Impostare un'autorità di certificazione</span><span class="sxs-lookup"><span data-stu-id="32347-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzKeyVaultCertificateOrganizationDetail -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="32347-111">Questo comando imposta le proprietà per un'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="32347-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="32347-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32347-112">PARAMETERS</span></span>

### <span data-ttu-id="32347-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="32347-113">-AccountId</span></span>
<span data-ttu-id="32347-114">Specifica l'ID account per l'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="32347-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32347-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="32347-115">-ApiKey</span></span>
<span data-ttu-id="32347-116">Specifica la chiave API per l'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="32347-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32347-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32347-117">-DefaultProfile</span></span>
<span data-ttu-id="32347-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="32347-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32347-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32347-119">-InputObject</span></span>
<span data-ttu-id="32347-120">Specifica l'autorità di certificazione da impostare.</span><span class="sxs-lookup"><span data-stu-id="32347-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32347-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="32347-121">-IssuerProvider</span></span>
<span data-ttu-id="32347-122">Specifica il tipo di autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="32347-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32347-123">-Name</span><span class="sxs-lookup"><span data-stu-id="32347-123">-Name</span></span>
<span data-ttu-id="32347-124">Specifica il nome dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="32347-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32347-125">-Dettagli organizzazione</span><span class="sxs-lookup"><span data-stu-id="32347-125">-OrganizationDetails</span></span>
<span data-ttu-id="32347-126">Dettagli dell'organizzazione da usare con l'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="32347-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32347-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32347-127">-PassThru</span></span>
<span data-ttu-id="32347-128">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="32347-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="32347-129">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="32347-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="32347-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="32347-130">-VaultName</span></span>
<span data-ttu-id="32347-131">Specifica il nome del vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="32347-131">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32347-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32347-132">-Confirm</span></span>
<span data-ttu-id="32347-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32347-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32347-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32347-134">-WhatIf</span></span>
<span data-ttu-id="32347-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32347-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32347-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32347-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32347-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32347-137">CommonParameters</span></span>
<span data-ttu-id="32347-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32347-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32347-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="32347-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32347-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="32347-140">INPUTS</span></span>

### <span data-ttu-id="32347-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="32347-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="32347-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="32347-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="32347-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32347-143">OUTPUTS</span></span>

### <span data-ttu-id="32347-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="32347-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="32347-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="32347-145">NOTES</span></span>

## <span data-ttu-id="32347-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32347-146">RELATED LINKS</span></span>

[<span data-ttu-id="32347-147">Get-AzKeyVaultCertificateIsssburg</span><span class="sxs-lookup"><span data-stu-id="32347-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="32347-148">Remove-AzKeyVaultCertificateIsssburg</span><span class="sxs-lookup"><span data-stu-id="32347-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

