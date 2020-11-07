---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: 05bd6c804d359a06e83f25922263bdfdb55acc73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676586"
---
# <span data-ttu-id="2fcd1-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2fcd1-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="2fcd1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fcd1-102">SYNOPSIS</span></span>
<span data-ttu-id="2fcd1-103">Rigenera una chiave di archiviazione per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2fcd1-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="2fcd1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fcd1-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fcd1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fcd1-105">DESCRIPTION</span></span>
<span data-ttu-id="2fcd1-106">Il cmdlet **New-AzStorageAccountKey** rigenera una chiave di archiviazione per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2fcd1-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="2fcd1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fcd1-107">EXAMPLES</span></span>

### <span data-ttu-id="2fcd1-108">Esempio 1: rigenerare una chiave di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2fcd1-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="2fcd1-109">Questo comando rigenera una chiave di archiviazione per l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="2fcd1-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="2fcd1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fcd1-110">PARAMETERS</span></span>

### <span data-ttu-id="2fcd1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fcd1-111">-DefaultProfile</span></span>
<span data-ttu-id="2fcd1-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2fcd1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fcd1-113">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="2fcd1-113">-KeyName</span></span>
<span data-ttu-id="2fcd1-114">Specifica il tasto da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="2fcd1-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="2fcd1-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2fcd1-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2fcd1-116">Key1</span><span class="sxs-lookup"><span data-stu-id="2fcd1-116">key1</span></span>
- <span data-ttu-id="2fcd1-117">Key2</span><span class="sxs-lookup"><span data-stu-id="2fcd1-117">key2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fcd1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fcd1-118">-Name</span></span>
<span data-ttu-id="2fcd1-119">Specifica il nome dell'account di archiviazione per cui rigenerare una chiave di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2fcd1-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="2fcd1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fcd1-120">-ResourceGroupName</span></span>
<span data-ttu-id="2fcd1-121">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2fcd1-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="2fcd1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fcd1-122">CommonParameters</span></span>
<span data-ttu-id="2fcd1-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fcd1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fcd1-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fcd1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fcd1-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fcd1-125">INPUTS</span></span>

### <span data-ttu-id="2fcd1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2fcd1-126">System.String</span></span>

## <span data-ttu-id="2fcd1-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fcd1-127">OUTPUTS</span></span>

### <span data-ttu-id="2fcd1-128">Microsoft. Azure. Management. storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2fcd1-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="2fcd1-129">Note</span><span class="sxs-lookup"><span data-stu-id="2fcd1-129">NOTES</span></span>

## <span data-ttu-id="2fcd1-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fcd1-130">RELATED LINKS</span></span>

[<span data-ttu-id="2fcd1-131">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2fcd1-131">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
