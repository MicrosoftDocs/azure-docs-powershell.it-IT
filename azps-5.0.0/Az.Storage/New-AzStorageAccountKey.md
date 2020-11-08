---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: eebf58120449466ac18231af6daed538ff7da937
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200650"
---
# <span data-ttu-id="ded21-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ded21-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="ded21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ded21-102">SYNOPSIS</span></span>
<span data-ttu-id="ded21-103">Rigenera una chiave di archiviazione per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ded21-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="ded21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ded21-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ded21-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ded21-105">DESCRIPTION</span></span>
<span data-ttu-id="ded21-106">Il cmdlet **New-AzStorageAccountKey** rigenera una chiave di archiviazione per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ded21-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="ded21-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ded21-107">EXAMPLES</span></span>

### <span data-ttu-id="ded21-108">Esempio 1: rigenerare una chiave di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ded21-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="ded21-109">Questo comando rigenera una chiave di archiviazione per l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="ded21-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="ded21-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ded21-110">PARAMETERS</span></span>

### <span data-ttu-id="ded21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ded21-111">-DefaultProfile</span></span>
<span data-ttu-id="ded21-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ded21-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ded21-113">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="ded21-113">-KeyName</span></span>
<span data-ttu-id="ded21-114">Specifica il tasto da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="ded21-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="ded21-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ded21-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ded21-116">Key1</span><span class="sxs-lookup"><span data-stu-id="ded21-116">key1</span></span>
- <span data-ttu-id="ded21-117">Key2</span><span class="sxs-lookup"><span data-stu-id="ded21-117">key2</span></span>
- <span data-ttu-id="ded21-118">kerb1</span><span class="sxs-lookup"><span data-stu-id="ded21-118">kerb1</span></span>
- <span data-ttu-id="ded21-119">kerb2</span><span class="sxs-lookup"><span data-stu-id="ded21-119">kerb2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2, kerb1, kerb2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ded21-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ded21-120">-Name</span></span>
<span data-ttu-id="ded21-121">Specifica il nome dell'account di archiviazione per cui rigenerare una chiave di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ded21-121">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="ded21-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ded21-122">-ResourceGroupName</span></span>
<span data-ttu-id="ded21-123">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ded21-123">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="ded21-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded21-124">CommonParameters</span></span>
<span data-ttu-id="ded21-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ded21-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ded21-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ded21-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded21-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ded21-127">INPUTS</span></span>

### <span data-ttu-id="ded21-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ded21-128">System.String</span></span>

## <span data-ttu-id="ded21-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ded21-129">OUTPUTS</span></span>

### <span data-ttu-id="ded21-130">Microsoft. Azure. Management. storage. Models. StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="ded21-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="ded21-131">Note</span><span class="sxs-lookup"><span data-stu-id="ded21-131">NOTES</span></span>

## <span data-ttu-id="ded21-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ded21-132">RELATED LINKS</span></span>

[<span data-ttu-id="ded21-133">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ded21-133">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)