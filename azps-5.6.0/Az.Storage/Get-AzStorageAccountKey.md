---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: cd540965b4de64b5fbdc5158faedf00f7a3516b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002798"
---
# <span data-ttu-id="90089-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="90089-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="90089-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90089-102">SYNOPSIS</span></span>
<span data-ttu-id="90089-103">Ottiene le chiavi di accesso per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="90089-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="90089-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90089-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90089-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="90089-105">DESCRIPTION</span></span>
<span data-ttu-id="90089-106">Il cmdlet **Get-AzStorageAccountKey** ottiene le chiavi di accesso per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="90089-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="90089-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90089-107">EXAMPLES</span></span>

### <span data-ttu-id="90089-108">Esempio 1: Ottenere le chiavi di accesso per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="90089-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="90089-109">Questo comando recupera le chiavi per l'account di archiviazione di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="90089-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="90089-110">Esempio 2: Ottenere una chiave di accesso specifica per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="90089-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="90089-111">Esempio 3: Elenca le chiavi di accesso per un account di archiviazione, includere le chiavi Kerberos (se Active Directory è abilitata)</span><span class="sxs-lookup"><span data-stu-id="90089-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="90089-112">Questo comando recupera le chiavi per l'account di archiviazione di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="90089-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="90089-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90089-113">PARAMETERS</span></span>

### <span data-ttu-id="90089-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90089-114">-DefaultProfile</span></span>
<span data-ttu-id="90089-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="90089-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90089-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="90089-116">-ListKerbKey</span></span>
<span data-ttu-id="90089-117">Elenca le chiavi Kerberos (se Active Directory è abilitata) per l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="90089-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="90089-118">La chiave Kerberos viene generata per ogni account di archiviazione per l'autenticazione basata sulle identità dei file di Azure con Servizio di dominio Azure Active Directory o Servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="90089-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="90089-119">Viene usata come password dell'identità registrata nel servizio di dominio che rappresenta l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="90089-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="90089-120">La chiave Kerberos non fornisce l'autorizzazione di accesso per eseguire operazioni di lettura o scrittura in aereo o di controllo sull'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="90089-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

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

### <span data-ttu-id="90089-121">-Name</span><span class="sxs-lookup"><span data-stu-id="90089-121">-Name</span></span>
<span data-ttu-id="90089-122">Specifica il nome dell'account di archiviazione per cui il cmdlet ottiene le chiavi.</span><span class="sxs-lookup"><span data-stu-id="90089-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90089-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90089-123">-ResourceGroupName</span></span>
<span data-ttu-id="90089-124">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="90089-124">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90089-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90089-125">CommonParameters</span></span>
<span data-ttu-id="90089-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90089-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90089-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90089-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90089-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="90089-128">INPUTS</span></span>

### <span data-ttu-id="90089-129">System.String</span><span class="sxs-lookup"><span data-stu-id="90089-129">System.String</span></span>

## <span data-ttu-id="90089-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90089-130">OUTPUTS</span></span>

### <span data-ttu-id="90089-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="90089-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="90089-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="90089-132">NOTES</span></span>

## <span data-ttu-id="90089-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90089-133">RELATED LINKS</span></span>

[<span data-ttu-id="90089-134">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="90089-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


