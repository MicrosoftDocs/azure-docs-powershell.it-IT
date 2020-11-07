---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 97faf51b25ee2ae36b028e4a6b992416949a219f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863017"
---
# <span data-ttu-id="1c826-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="1c826-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="1c826-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c826-102">SYNOPSIS</span></span>
<span data-ttu-id="1c826-103">Imposta l'emittente di un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="1c826-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="1c826-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c826-104">SYNTAX</span></span>

### <span data-ttu-id="1c826-105">Espanso (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c826-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c826-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="1c826-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c826-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c826-107">DESCRIPTION</span></span>
<span data-ttu-id="1c826-108">Il cmdlet Set-AzKeyVaultCertificateIssuer imposta un emittente di certificati in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="1c826-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="1c826-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c826-109">EXAMPLES</span></span>

### <span data-ttu-id="1c826-110">Esempio 1: impostare un emittente di certificati</span><span class="sxs-lookup"><span data-stu-id="1c826-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="1c826-111">Questo comando imposta le proprietà per un emittente di certificati e lo archivia nella variabile $Issuer.</span><span class="sxs-lookup"><span data-stu-id="1c826-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="1c826-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c826-112">PARAMETERS</span></span>

### <span data-ttu-id="1c826-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="1c826-113">-AccountId</span></span>
<span data-ttu-id="1c826-114">Specifica l'ID account dell'autorità di certificazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="1c826-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c826-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="1c826-115">-ApiKey</span></span>
<span data-ttu-id="1c826-116">Specifica la chiave API per l'emittente del certificato.</span><span class="sxs-lookup"><span data-stu-id="1c826-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: SecureString
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c826-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c826-117">-DefaultProfile</span></span>
<span data-ttu-id="1c826-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1c826-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c826-119">-Emittente</span><span class="sxs-lookup"><span data-stu-id="1c826-119">-Issuer</span></span>
<span data-ttu-id="1c826-120">Specifica l'emittente del certificato da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="1c826-120">Specifies the certificate issuer to update.</span></span>

```yaml
Type: KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c826-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="1c826-121">-IssuerProvider</span></span>
<span data-ttu-id="1c826-122">Specifica il tipo di autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="1c826-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c826-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c826-123">-Name</span></span>
<span data-ttu-id="1c826-124">Specifica il nome dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="1c826-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c826-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="1c826-125">-OrganizationDetails</span></span>
<span data-ttu-id="1c826-126">Dettagli dell'organizzazione da usare con l'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="1c826-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c826-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c826-127">-PassThru</span></span>
<span data-ttu-id="1c826-128">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="1c826-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1c826-129">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="1c826-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1c826-130">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="1c826-130">-VaultName</span></span>
<span data-ttu-id="1c826-131">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="1c826-131">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c826-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1c826-132">-Confirm</span></span>
<span data-ttu-id="1c826-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c826-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c826-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c826-134">-WhatIf</span></span>
<span data-ttu-id="1c826-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c826-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c826-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c826-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c826-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c826-137">CommonParameters</span></span>
<span data-ttu-id="1c826-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c826-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c826-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c826-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c826-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c826-140">INPUTS</span></span>

### <span data-ttu-id="1c826-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1c826-141">None</span></span>
<span data-ttu-id="1c826-142">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1c826-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c826-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c826-143">OUTPUTS</span></span>

### <span data-ttu-id="1c826-144">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1c826-144">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="1c826-145">Note</span><span class="sxs-lookup"><span data-stu-id="1c826-145">NOTES</span></span>

## <span data-ttu-id="1c826-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c826-146">RELATED LINKS</span></span>

[<span data-ttu-id="1c826-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="1c826-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="1c826-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="1c826-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

