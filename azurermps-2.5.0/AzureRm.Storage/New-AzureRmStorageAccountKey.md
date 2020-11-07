---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccountkey
schema: 2.0.0
ms.openlocfilehash: 7ea3847c011582d9be809f030a638b09b6cf9532
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865715"
---
# <span data-ttu-id="01184-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="01184-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="01184-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01184-102">SYNOPSIS</span></span>
<span data-ttu-id="01184-103">Rigenera una chiave di archiviazione per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="01184-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01184-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01184-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01184-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01184-105">DESCRIPTION</span></span>
<span data-ttu-id="01184-106">Il cmdlet **New-AzureRmStorageAccountKey** rigenera una chiave di archiviazione per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="01184-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="01184-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01184-107">EXAMPLES</span></span>

### <span data-ttu-id="01184-108">Esempio 1: rigenerare una chiave di archiviazione</span><span class="sxs-lookup"><span data-stu-id="01184-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="01184-109">Questo comando rigenera una chiave di archiviazione per l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="01184-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="01184-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01184-110">PARAMETERS</span></span>

### <span data-ttu-id="01184-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01184-111">-DefaultProfile</span></span>
<span data-ttu-id="01184-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01184-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01184-113">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="01184-113">-KeyName</span></span>
<span data-ttu-id="01184-114">Specifica il tasto da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="01184-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="01184-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="01184-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="01184-116">Key1</span><span class="sxs-lookup"><span data-stu-id="01184-116">key1</span></span>
- <span data-ttu-id="01184-117">Key2</span><span class="sxs-lookup"><span data-stu-id="01184-117">key2</span></span>

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

### <span data-ttu-id="01184-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="01184-118">-Name</span></span>
<span data-ttu-id="01184-119">Specifica il nome dell'account di archiviazione per cui rigenerare una chiave di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="01184-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="01184-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01184-120">-ResourceGroupName</span></span>
<span data-ttu-id="01184-121">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="01184-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="01184-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01184-122">CommonParameters</span></span>
<span data-ttu-id="01184-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01184-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01184-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01184-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01184-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01184-125">INPUTS</span></span>

### <span data-ttu-id="01184-126">System. String</span><span class="sxs-lookup"><span data-stu-id="01184-126">System.String</span></span>

## <span data-ttu-id="01184-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01184-127">OUTPUTS</span></span>

### <span data-ttu-id="01184-128">Microsoft. Azure. Management. storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="01184-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="01184-129">Note</span><span class="sxs-lookup"><span data-stu-id="01184-129">NOTES</span></span>

## <span data-ttu-id="01184-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01184-130">RELATED LINKS</span></span>

[<span data-ttu-id="01184-131">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="01184-131">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
