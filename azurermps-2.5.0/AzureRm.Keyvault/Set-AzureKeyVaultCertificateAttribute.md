---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateattribute
schema: 2.0.0
ms.openlocfilehash: 9f7c08f42026c6cc5d321ae78687a903c8393904
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865779"
---
# <span data-ttu-id="d95c0-101">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="d95c0-101">Set-AzureKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="d95c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d95c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d95c0-103">Modifica gli attributi modificabili di un certificato.</span><span class="sxs-lookup"><span data-stu-id="d95c0-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d95c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d95c0-104">SYNTAX</span></span>

```
Set-AzureKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d95c0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d95c0-105">DESCRIPTION</span></span>
<span data-ttu-id="d95c0-106">Il cmdlet **set-AzureKeyVaultCertificateAttribute** modifica gli attributi modificabili di un certificato.</span><span class="sxs-lookup"><span data-stu-id="d95c0-106">The **Set-AzureKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="d95c0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d95c0-107">EXAMPLES</span></span>

### <span data-ttu-id="d95c0-108">Esempio 1: modificare i tag associati a un certificato</span><span class="sxs-lookup"><span data-stu-id="d95c0-108">Example 1: Modify the tags associated with a certificate</span></span>
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzureKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : "TestCert01"
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                5A2EF60501F241D6A4336841B36FEA41

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                A565D568082FEE2BE33B356ECC3703C2E9886555

Id          : https://ContosoKV01.vault.azure.net:443/certificates/tt02
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/tt02
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/tt02
Thumbprint  : A565D568082FEE2BE33B356ECC3703C2E9886555
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="d95c0-109">Il primo comando assegna una matrice di coppie chiave/valore alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="d95c0-109">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="d95c0-110">Il secondo comando imposta il valore di tag del certificato denominato TestCert01 $Tags.</span><span class="sxs-lookup"><span data-stu-id="d95c0-110">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="d95c0-111">Il comando finale Visualizza il certificato TestCert01 usando il cmdlet Get-AzureKeyVaultCertificate per verificare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d95c0-111">The final command displays the TestCert01 certificate by using the Get-AzureKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="d95c0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d95c0-112">PARAMETERS</span></span>

### <span data-ttu-id="d95c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d95c0-113">-DefaultProfile</span></span>
<span data-ttu-id="d95c0-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d95c0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d95c0-115">-Enable</span><span class="sxs-lookup"><span data-stu-id="d95c0-115">-Enable</span></span>
<span data-ttu-id="d95c0-116">Indica se abilitare o disabilitare un certificato.</span><span class="sxs-lookup"><span data-stu-id="d95c0-116">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="d95c0-117">Specificare $True per abilitare o $False per disabilitare.</span><span class="sxs-lookup"><span data-stu-id="d95c0-117">Specify $True to enable or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d95c0-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d95c0-118">-Name</span></span>
<span data-ttu-id="d95c0-119">Specifica il nome del certificato da modificare.</span><span class="sxs-lookup"><span data-stu-id="d95c0-119">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="d95c0-120">Questo cmdlet costruisce il nome di dominio completo di un certificato basato sul nome del Vault della chiave, sull'ambiente attualmente selezionato, su quello del certificato e sulla versione del certificato.</span><span class="sxs-lookup"><span data-stu-id="d95c0-120">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d95c0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d95c0-121">-PassThru</span></span>
<span data-ttu-id="d95c0-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="d95c0-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d95c0-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d95c0-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d95c0-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="d95c0-124">-Tag</span></span>
<span data-ttu-id="d95c0-125">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d95c0-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d95c0-126">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="d95c0-126">For example:</span></span>

<span data-ttu-id="d95c0-127">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d95c0-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d95c0-128">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="d95c0-128">-VaultName</span></span>
<span data-ttu-id="d95c0-129">Specifica il nome del Vault chiave in cui questo cmdlet modifica un certificato.</span><span class="sxs-lookup"><span data-stu-id="d95c0-129">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="d95c0-130">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="d95c0-130">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d95c0-131">-Versione</span><span class="sxs-lookup"><span data-stu-id="d95c0-131">-Version</span></span>
<span data-ttu-id="d95c0-132">Specifica la versione di un certificato.</span><span class="sxs-lookup"><span data-stu-id="d95c0-132">Specifies the version of a certificate.</span></span>
<span data-ttu-id="d95c0-133">Questo cmdlet costruisce il nome di dominio completo di un certificato basato sul nome del Vault della chiave, sull'ambiente attualmente selezionato, su quello del certificato e sulla versione del certificato.</span><span class="sxs-lookup"><span data-stu-id="d95c0-133">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d95c0-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d95c0-134">-Confirm</span></span>
<span data-ttu-id="d95c0-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d95c0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d95c0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d95c0-136">-WhatIf</span></span>
<span data-ttu-id="d95c0-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d95c0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d95c0-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d95c0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d95c0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d95c0-139">CommonParameters</span></span>
<span data-ttu-id="d95c0-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d95c0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d95c0-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d95c0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d95c0-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d95c0-142">INPUTS</span></span>

## <span data-ttu-id="d95c0-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d95c0-143">OUTPUTS</span></span>

### <span data-ttu-id="d95c0-144">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d95c0-144">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="d95c0-145">Note</span><span class="sxs-lookup"><span data-stu-id="d95c0-145">NOTES</span></span>

## <span data-ttu-id="d95c0-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d95c0-146">RELATED LINKS</span></span>

[<span data-ttu-id="d95c0-147">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d95c0-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)
