---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 4d3be232e97f71a030548fd0b3754a7472b80b22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189846"
---
# <span data-ttu-id="3fdc0-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3fdc0-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="3fdc0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3fdc0-102">SYNOPSIS</span></span>
<span data-ttu-id="3fdc0-103">Imposta l'emittente di un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="3fdc0-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="3fdc0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3fdc0-104">SYNTAX</span></span>

### <span data-ttu-id="3fdc0-105">Espanso (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3fdc0-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fdc0-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="3fdc0-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fdc0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fdc0-107">DESCRIPTION</span></span>
<span data-ttu-id="3fdc0-108">Il cmdlet Set-AzKeyVaultCertificateIssuer imposta un emittente di certificati in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="3fdc0-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="3fdc0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3fdc0-109">EXAMPLES</span></span>

### <span data-ttu-id="3fdc0-110">Esempio 1: impostare un emittente di certificati</span><span class="sxs-lookup"><span data-stu-id="3fdc0-110">Example 1: Set a certificate issuer</span></span>
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

<span data-ttu-id="3fdc0-111">Questo comando imposta le proprietà per un emittente di certificati.</span><span class="sxs-lookup"><span data-stu-id="3fdc0-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="3fdc0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3fdc0-112">PARAMETERS</span></span>

### <span data-ttu-id="3fdc0-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="3fdc0-113">-AccountId</span></span>
<span data-ttu-id="3fdc0-114">Specifica l'ID account dell'autorità di certificazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="3fdc0-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="3fdc0-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="3fdc0-115">-ApiKey</span></span>
<span data-ttu-id="3fdc0-116">Specifica la chiave API per l'emittente del certificato.</span><span class="sxs-lookup"><span data-stu-id="3fdc0-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="3fdc0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fdc0-117">-DefaultProfile</span></span>
<span data-ttu-id="3fdc0-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3fdc0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fdc0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fdc0-119">-InputObject</span></span>
<span data-ttu-id="3fdc0-120">Specifica l'emittente del certificato da impostare.</span><span class="sxs-lookup"><span data-stu-id="3fdc0-120">Specifies the certificate issuer to set.</span></span>

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

### <span data-ttu-id="3fdc0-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="3fdc0-121">-IssuerProvider</span></span>
<span data-ttu-id="3fdc0-122">Specifica il tipo di autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="3fdc0-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="3fdc0-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="3fdc0-123">-Name</span></span>
<span data-ttu-id="3fdc0-124">Specifica il nome dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="3fdc0-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="3fdc0-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="3fdc0-125">-OrganizationDetails</span></span>
<span data-ttu-id="3fdc0-126">Dettagli dell'organizzazione da usare con l'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="3fdc0-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="3fdc0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fdc0-127">-PassThru</span></span>
<span data-ttu-id="3fdc0-128">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="3fdc0-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3fdc0-129">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="3fdc0-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3fdc0-130">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="3fdc0-130">-VaultName</span></span>
<span data-ttu-id="3fdc0-131">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="3fdc0-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="3fdc0-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3fdc0-132">-Confirm</span></span>
<span data-ttu-id="3fdc0-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fdc0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fdc0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fdc0-134">-WhatIf</span></span>
<span data-ttu-id="3fdc0-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3fdc0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fdc0-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3fdc0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fdc0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fdc0-137">CommonParameters</span></span>
<span data-ttu-id="3fdc0-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fdc0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fdc0-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fdc0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fdc0-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3fdc0-140">INPUTS</span></span>

### <span data-ttu-id="3fdc0-141">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="3fdc0-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="3fdc0-142">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3fdc0-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="3fdc0-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3fdc0-143">OUTPUTS</span></span>

### <span data-ttu-id="3fdc0-144">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3fdc0-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="3fdc0-145">Note</span><span class="sxs-lookup"><span data-stu-id="3fdc0-145">NOTES</span></span>

## <span data-ttu-id="3fdc0-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3fdc0-146">RELATED LINKS</span></span>

[<span data-ttu-id="3fdc0-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3fdc0-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="3fdc0-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3fdc0-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

