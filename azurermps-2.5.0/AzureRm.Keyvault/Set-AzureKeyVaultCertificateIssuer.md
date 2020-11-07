---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: 430a909e76c08ba0c19c18072fdf019cd2fa7b29
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866510"
---
# <span data-ttu-id="42bc5-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="42bc5-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="42bc5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="42bc5-103">Imposta l'emittente di un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="42bc5-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42bc5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42bc5-104">SYNTAX</span></span>

### <span data-ttu-id="42bc5-105">Espanso (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="42bc5-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42bc5-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="42bc5-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42bc5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42bc5-107">DESCRIPTION</span></span>
<span data-ttu-id="42bc5-108">Il cmdlet Set-AzureKeyVaultCertificateIssuer imposta un emittente di certificati in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="42bc5-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="42bc5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42bc5-109">EXAMPLES</span></span>

### <span data-ttu-id="42bc5-110">Esempio 1: impostare un emittente di certificati</span><span class="sxs-lookup"><span data-stu-id="42bc5-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="42bc5-111">Questo comando imposta le proprietà per un emittente di certificati e lo archivia nella variabile $Issuer.</span><span class="sxs-lookup"><span data-stu-id="42bc5-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="42bc5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42bc5-112">PARAMETERS</span></span>

### <span data-ttu-id="42bc5-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="42bc5-113">-AccountId</span></span>
<span data-ttu-id="42bc5-114">Specifica l'ID account dell'autorità di certificazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="42bc5-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="42bc5-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="42bc5-115">-ApiKey</span></span>
<span data-ttu-id="42bc5-116">Specifica la chiave API per l'emittente del certificato.</span><span class="sxs-lookup"><span data-stu-id="42bc5-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="42bc5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42bc5-117">-DefaultProfile</span></span>
<span data-ttu-id="42bc5-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="42bc5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42bc5-119">-Emittente</span><span class="sxs-lookup"><span data-stu-id="42bc5-119">-Issuer</span></span>
<span data-ttu-id="42bc5-120">Specifica l'emittente del certificato da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="42bc5-120">Specifies the certificate issuer to update.</span></span>

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

### <span data-ttu-id="42bc5-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="42bc5-121">-IssuerProvider</span></span>
<span data-ttu-id="42bc5-122">Specifica il tipo di autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="42bc5-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="42bc5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="42bc5-123">-Name</span></span>
<span data-ttu-id="42bc5-124">Specifica il nome dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="42bc5-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="42bc5-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="42bc5-125">-OrganizationDetails</span></span>
<span data-ttu-id="42bc5-126">Dettagli dell'organizzazione da usare con l'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="42bc5-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="42bc5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42bc5-127">-PassThru</span></span>
<span data-ttu-id="42bc5-128">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="42bc5-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="42bc5-129">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="42bc5-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="42bc5-130">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="42bc5-130">-VaultName</span></span>
<span data-ttu-id="42bc5-131">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="42bc5-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="42bc5-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="42bc5-132">-Confirm</span></span>
<span data-ttu-id="42bc5-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42bc5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42bc5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42bc5-134">-WhatIf</span></span>
<span data-ttu-id="42bc5-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42bc5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42bc5-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42bc5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42bc5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42bc5-137">CommonParameters</span></span>
<span data-ttu-id="42bc5-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42bc5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42bc5-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42bc5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42bc5-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42bc5-140">INPUTS</span></span>

## <span data-ttu-id="42bc5-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42bc5-141">OUTPUTS</span></span>

### <span data-ttu-id="42bc5-142">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="42bc5-142">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="42bc5-143">Note</span><span class="sxs-lookup"><span data-stu-id="42bc5-143">NOTES</span></span>

## <span data-ttu-id="42bc5-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42bc5-144">RELATED LINKS</span></span>

[<span data-ttu-id="42bc5-145">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="42bc5-145">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="42bc5-146">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="42bc5-146">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

