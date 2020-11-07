---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: e02b60055818d1ed79e93e6853353795e78c5830
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861318"
---
# <span data-ttu-id="b8d3c-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b8d3c-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="b8d3c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8d3c-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d3c-103">Ottiene i contatti registrati per le notifiche dei certificati per un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="b8d3c-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="b8d3c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8d3c-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8d3c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8d3c-105">DESCRIPTION</span></span>
<span data-ttu-id="b8d3c-106">Il cmdlet **Get-AzKeyVaultCertificateContact** ottiene i contatti registrati per le notifiche dei certificati per un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="b8d3c-106">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="b8d3c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8d3c-107">EXAMPLES</span></span>

### <span data-ttu-id="b8d3c-108">Esempio 1: ottenere tutti i contatti dei certificati</span><span class="sxs-lookup"><span data-stu-id="b8d3c-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="b8d3c-109">Questo comando consente di ottenere tutti i contatti per gli oggetti certificato nel caveau della chiave Contoso e quindi di archiviarli nella variabile $Contacts.</span><span class="sxs-lookup"><span data-stu-id="b8d3c-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="b8d3c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8d3c-110">PARAMETERS</span></span>

### <span data-ttu-id="b8d3c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d3c-111">-DefaultProfile</span></span>
<span data-ttu-id="b8d3c-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b8d3c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8d3c-113">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="b8d3c-113">-VaultName</span></span>
<span data-ttu-id="b8d3c-114">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="b8d3c-114">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="b8d3c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d3c-115">CommonParameters</span></span>
<span data-ttu-id="b8d3c-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8d3c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d3c-117">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8d3c-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d3c-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8d3c-118">INPUTS</span></span>

### <span data-ttu-id="b8d3c-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b8d3c-119">None</span></span>
<span data-ttu-id="b8d3c-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b8d3c-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b8d3c-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8d3c-121">OUTPUTS</span></span>

### <span data-ttu-id="b8d3c-122">Elenco<Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="b8d3c-122">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="b8d3c-123">Note</span><span class="sxs-lookup"><span data-stu-id="b8d3c-123">NOTES</span></span>

## <span data-ttu-id="b8d3c-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8d3c-124">RELATED LINKS</span></span>

[<span data-ttu-id="b8d3c-125">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b8d3c-125">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="b8d3c-126">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b8d3c-126">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

