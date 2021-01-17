---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ca7f0f87ebcbad3d613939f2e73a743763b134c9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323520"
---
# <span data-ttu-id="79277-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="79277-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="79277-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79277-102">SYNOPSIS</span></span>
<span data-ttu-id="79277-103">Ottiene i contatti registrati per le notifiche dei certificati per un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="79277-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="79277-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79277-104">SYNTAX</span></span>

### <span data-ttu-id="79277-105">VAULTNAME (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="79277-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79277-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="79277-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79277-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="79277-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79277-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79277-108">DESCRIPTION</span></span>
<span data-ttu-id="79277-109">Il cmdlet **Get-AzKeyVaultCertificateContact** ottiene i contatti registrati per le notifiche dei certificati per un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="79277-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="79277-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79277-110">EXAMPLES</span></span>

### <span data-ttu-id="79277-111">Esempio 1: ottenere tutti i contatti dei certificati</span><span class="sxs-lookup"><span data-stu-id="79277-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="79277-112">Questo comando consente di ottenere tutti i contatti per gli oggetti certificato nel caveau della chiave Contoso e quindi di archiviarli nella variabile $Contacts.</span><span class="sxs-lookup"><span data-stu-id="79277-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="79277-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79277-113">PARAMETERS</span></span>

### <span data-ttu-id="79277-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79277-114">-DefaultProfile</span></span>
<span data-ttu-id="79277-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="79277-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79277-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79277-116">-InputObject</span></span>
<span data-ttu-id="79277-117">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="79277-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79277-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79277-118">-ResourceId</span></span>
<span data-ttu-id="79277-119">ID del Vault.</span><span class="sxs-lookup"><span data-stu-id="79277-119">KeyVault Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79277-120">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="79277-120">-VaultName</span></span>
<span data-ttu-id="79277-121">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="79277-121">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79277-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79277-122">CommonParameters</span></span>
<span data-ttu-id="79277-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79277-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79277-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79277-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79277-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79277-125">INPUTS</span></span>

### <span data-ttu-id="79277-126">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="79277-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="79277-127">System. String</span><span class="sxs-lookup"><span data-stu-id="79277-127">System.String</span></span>

## <span data-ttu-id="79277-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79277-128">OUTPUTS</span></span>

### <span data-ttu-id="79277-129">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="79277-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="79277-130">Note</span><span class="sxs-lookup"><span data-stu-id="79277-130">NOTES</span></span>

## <span data-ttu-id="79277-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79277-131">RELATED LINKS</span></span>

[<span data-ttu-id="79277-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="79277-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="79277-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="79277-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

