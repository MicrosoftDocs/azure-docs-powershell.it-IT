---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 9c7b82c8ec884cc16bc3c593d9f00f1789b98e52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674162"
---
# <span data-ttu-id="e7176-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e7176-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e7176-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e7176-102">SYNOPSIS</span></span>
<span data-ttu-id="e7176-103">Ottiene i contatti registrati per le notifiche dei certificati per un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="e7176-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="e7176-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7176-104">SYNTAX</span></span>

### <span data-ttu-id="e7176-105">VAULTNAME (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e7176-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7176-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e7176-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7176-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7176-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7176-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7176-108">DESCRIPTION</span></span>
<span data-ttu-id="e7176-109">Il cmdlet **Get-AzKeyVaultCertificateContact** ottiene i contatti registrati per le notifiche dei certificati per un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e7176-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="e7176-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7176-110">EXAMPLES</span></span>

### <span data-ttu-id="e7176-111">Esempio 1: ottenere tutti i contatti dei certificati</span><span class="sxs-lookup"><span data-stu-id="e7176-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="e7176-112">Questo comando consente di ottenere tutti i contatti per gli oggetti certificato nel caveau della chiave Contoso e quindi di archiviarli nella variabile $Contacts.</span><span class="sxs-lookup"><span data-stu-id="e7176-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="e7176-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e7176-113">PARAMETERS</span></span>

### <span data-ttu-id="e7176-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7176-114">-DefaultProfile</span></span>
<span data-ttu-id="e7176-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e7176-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7176-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7176-116">-InputObject</span></span>
<span data-ttu-id="e7176-117">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="e7176-117">KeyVault object.</span></span>

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

### <span data-ttu-id="e7176-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7176-118">-ResourceId</span></span>
<span data-ttu-id="e7176-119">ID del Vault.</span><span class="sxs-lookup"><span data-stu-id="e7176-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="e7176-120">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="e7176-120">-VaultName</span></span>
<span data-ttu-id="e7176-121">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="e7176-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="e7176-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7176-122">CommonParameters</span></span>
<span data-ttu-id="e7176-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7176-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7176-124">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7176-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7176-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e7176-125">INPUTS</span></span>

### <span data-ttu-id="e7176-126">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e7176-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e7176-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e7176-127">System.String</span></span>

## <span data-ttu-id="e7176-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7176-128">OUTPUTS</span></span>

### <span data-ttu-id="e7176-129">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e7176-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e7176-130">Note</span><span class="sxs-lookup"><span data-stu-id="e7176-130">NOTES</span></span>

## <span data-ttu-id="e7176-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7176-131">RELATED LINKS</span></span>

[<span data-ttu-id="e7176-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e7176-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="e7176-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e7176-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

