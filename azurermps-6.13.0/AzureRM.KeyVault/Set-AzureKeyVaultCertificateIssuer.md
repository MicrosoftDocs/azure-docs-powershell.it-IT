---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 69619b9f5ddd54e0d307a096cc967c307d1f36d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510959"
---
# <span data-ttu-id="6b95c-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6b95c-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="6b95c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b95c-102">SYNOPSIS</span></span>
<span data-ttu-id="6b95c-103">Imposta l'emittente di un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="6b95c-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b95c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b95c-104">SYNTAX</span></span>

### <span data-ttu-id="6b95c-105">Espanso (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6b95c-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b95c-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="6b95c-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b95c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b95c-107">DESCRIPTION</span></span>
<span data-ttu-id="6b95c-108">Il cmdlet Set-AzureKeyVaultCertificateIssuer imposta un emittente di certificati in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="6b95c-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="6b95c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b95c-109">EXAMPLES</span></span>

### <span data-ttu-id="6b95c-110">Esempio 1: impostare un emittente di certificati</span><span class="sxs-lookup"><span data-stu-id="6b95c-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="6b95c-111">Questo comando imposta le proprietà per un emittente di certificati.</span><span class="sxs-lookup"><span data-stu-id="6b95c-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="6b95c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b95c-112">PARAMETERS</span></span>

### <span data-ttu-id="6b95c-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="6b95c-113">-AccountId</span></span>
<span data-ttu-id="6b95c-114">Specifica l'ID account dell'autorità di certificazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="6b95c-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="6b95c-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="6b95c-115">-ApiKey</span></span>
<span data-ttu-id="6b95c-116">Specifica la chiave API per l'emittente del certificato.</span><span class="sxs-lookup"><span data-stu-id="6b95c-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="6b95c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b95c-117">-DefaultProfile</span></span>
<span data-ttu-id="6b95c-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6b95c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b95c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b95c-119">-InputObject</span></span>
<span data-ttu-id="6b95c-120">Specifica l'emittente del certificato da impostare.</span><span class="sxs-lookup"><span data-stu-id="6b95c-120">Specifies the certificate issuer to set.</span></span>

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

### <span data-ttu-id="6b95c-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="6b95c-121">-IssuerProvider</span></span>
<span data-ttu-id="6b95c-122">Specifica il tipo di autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="6b95c-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="6b95c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b95c-123">-Name</span></span>
<span data-ttu-id="6b95c-124">Specifica il nome dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="6b95c-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="6b95c-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="6b95c-125">-OrganizationDetails</span></span>
<span data-ttu-id="6b95c-126">Dettagli dell'organizzazione da usare con l'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="6b95c-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="6b95c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b95c-127">-PassThru</span></span>
<span data-ttu-id="6b95c-128">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="6b95c-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6b95c-129">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="6b95c-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6b95c-130">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="6b95c-130">-VaultName</span></span>
<span data-ttu-id="6b95c-131">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="6b95c-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="6b95c-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b95c-132">-Confirm</span></span>
<span data-ttu-id="6b95c-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b95c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b95c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b95c-134">-WhatIf</span></span>
<span data-ttu-id="6b95c-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b95c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b95c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b95c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b95c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b95c-137">CommonParameters</span></span>
<span data-ttu-id="6b95c-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b95c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b95c-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b95c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b95c-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b95c-140">INPUTS</span></span>

### <span data-ttu-id="6b95c-141">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="6b95c-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>
<span data-ttu-id="6b95c-142">Parametri: OrganizationDetails (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b95c-142">Parameters: OrganizationDetails (ByValue)</span></span>

### <span data-ttu-id="6b95c-143">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6b95c-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>
<span data-ttu-id="6b95c-144">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b95c-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6b95c-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b95c-145">OUTPUTS</span></span>

### <span data-ttu-id="6b95c-146">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6b95c-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6b95c-147">Note</span><span class="sxs-lookup"><span data-stu-id="6b95c-147">NOTES</span></span>

## <span data-ttu-id="6b95c-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b95c-148">RELATED LINKS</span></span>

[<span data-ttu-id="6b95c-149">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6b95c-149">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="6b95c-150">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6b95c-150">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

