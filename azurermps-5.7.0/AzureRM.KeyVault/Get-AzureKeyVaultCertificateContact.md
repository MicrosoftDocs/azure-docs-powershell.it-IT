---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: cf60626ec04a2466fc9565aef5daff896281345d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685832"
---
# <span data-ttu-id="13bac-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="13bac-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="13bac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="13bac-102">SYNOPSIS</span></span>
<span data-ttu-id="13bac-103">Ottiene i contatti registrati per le notifiche dei certificati per un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="13bac-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13bac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13bac-104">SYNTAX</span></span>

### <span data-ttu-id="13bac-105">VAULTNAME (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="13bac-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13bac-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="13bac-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13bac-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="13bac-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13bac-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13bac-108">DESCRIPTION</span></span>
<span data-ttu-id="13bac-109">Il cmdlet **Get-AzureKeyVaultCertificateContact** ottiene i contatti registrati per le notifiche dei certificati per un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="13bac-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="13bac-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13bac-110">EXAMPLES</span></span>

### <span data-ttu-id="13bac-111">Esempio 1: ottenere tutti i contatti dei certificati</span><span class="sxs-lookup"><span data-stu-id="13bac-111">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="13bac-112">Questo comando consente di ottenere tutti i contatti per gli oggetti certificato nel caveau della chiave Contoso e quindi di archiviarli nella variabile $Contacts.</span><span class="sxs-lookup"><span data-stu-id="13bac-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="13bac-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="13bac-113">PARAMETERS</span></span>

### <span data-ttu-id="13bac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13bac-114">-DefaultProfile</span></span>
<span data-ttu-id="13bac-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="13bac-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13bac-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13bac-116">-InputObject</span></span>
<span data-ttu-id="13bac-117">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="13bac-117">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13bac-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13bac-118">-ResourceId</span></span>
<span data-ttu-id="13bac-119">ID del Vault.</span><span class="sxs-lookup"><span data-stu-id="13bac-119">KeyVault Id.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13bac-120">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="13bac-120">-VaultName</span></span>
<span data-ttu-id="13bac-121">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="13bac-121">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13bac-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13bac-122">CommonParameters</span></span>
<span data-ttu-id="13bac-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13bac-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13bac-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13bac-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13bac-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="13bac-125">INPUTS</span></span>

### <span data-ttu-id="13bac-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="13bac-126">None</span></span>
<span data-ttu-id="13bac-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="13bac-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="13bac-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13bac-128">OUTPUTS</span></span>

### <span data-ttu-id="13bac-129">Elenco<Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="13bac-129">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="13bac-130">Note</span><span class="sxs-lookup"><span data-stu-id="13bac-130">NOTES</span></span>

## <span data-ttu-id="13bac-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13bac-131">RELATED LINKS</span></span>

[<span data-ttu-id="13bac-132">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="13bac-132">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="13bac-133">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="13bac-133">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

