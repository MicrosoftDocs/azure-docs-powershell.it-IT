---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191773"
---
# <span data-ttu-id="4c602-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4c602-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="4c602-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c602-102">SYNOPSIS</span></span>
<span data-ttu-id="4c602-103">Ottiene i tasti di scelta per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c602-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="4c602-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c602-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c602-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c602-105">DESCRIPTION</span></span>
<span data-ttu-id="4c602-106">Il cmdlet **Get-AzStorageAccountKey** ottiene i tasti di scelta per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c602-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="4c602-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c602-107">EXAMPLES</span></span>

### <span data-ttu-id="4c602-108">Esempio 1: ottenere i tasti di scelta per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4c602-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="4c602-109">Questo comando consente di ottenere le chiavi per l'account di archiviazione di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="4c602-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="4c602-110">Esempio 2: ottenere un tasto di accesso specifico per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4c602-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="4c602-111">Esempio 3: elenca i tasti di scelta per un account di archiviazione, include le chiavi Kerberos (se Active Directory è abilitato)</span><span class="sxs-lookup"><span data-stu-id="4c602-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="4c602-112">Questo comando consente di ottenere le chiavi per l'account di archiviazione di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="4c602-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="4c602-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c602-113">PARAMETERS</span></span>

### <span data-ttu-id="4c602-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c602-114">-DefaultProfile</span></span>
<span data-ttu-id="4c602-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c602-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c602-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="4c602-116">-ListKerbKey</span></span>
<span data-ttu-id="4c602-117">Elenca le chiavi Kerberos (se Active Directory è abilitato) per l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="4c602-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="4c602-118">La chiave Kerberos viene generata per ogni account di archiviazione per l'autenticazione basata su identità di file Azure con il servizio di dominio Azure Active Directory (Azure AD DS) o il servizio di dominio Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="4c602-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="4c602-119">Viene usata come password dell'identità registrata nel servizio del dominio che rappresenta l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4c602-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="4c602-120">La chiave Kerberos non offre l'autorizzazione di accesso per eseguire operazioni di lettura o scrittura in un piano di controllo o di dati sull'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4c602-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

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

### <span data-ttu-id="4c602-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c602-121">-Name</span></span>
<span data-ttu-id="4c602-122">Specifica il nome dell'account di archiviazione per cui questo cmdlet ottiene le chiavi.</span><span class="sxs-lookup"><span data-stu-id="4c602-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="4c602-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c602-123">-ResourceGroupName</span></span>
<span data-ttu-id="4c602-124">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4c602-124">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="4c602-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c602-125">CommonParameters</span></span>
<span data-ttu-id="4c602-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c602-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c602-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c602-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c602-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c602-128">INPUTS</span></span>

### <span data-ttu-id="4c602-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4c602-129">System.String</span></span>

## <span data-ttu-id="4c602-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c602-130">OUTPUTS</span></span>

### <span data-ttu-id="4c602-131">Microsoft. Azure. Management. storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4c602-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="4c602-132">Note</span><span class="sxs-lookup"><span data-stu-id="4c602-132">NOTES</span></span>

## <span data-ttu-id="4c602-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c602-133">RELATED LINKS</span></span>

[<span data-ttu-id="4c602-134">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4c602-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


