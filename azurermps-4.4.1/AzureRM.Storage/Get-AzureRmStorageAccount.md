---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: 07fdf5a05f5099facabb78f35c44856545d1efe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686022"
---
# <span data-ttu-id="ac4ab-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ac4ab-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="ac4ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac4ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ac4ab-103">Ottiene un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ac4ab-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac4ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac4ab-104">SYNTAX</span></span>

### <span data-ttu-id="ac4ab-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac4ab-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac4ab-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac4ab-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac4ab-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac4ab-107">DESCRIPTION</span></span>
<span data-ttu-id="ac4ab-108">Il cmdlet **Get-AzureRmStorageAccount** ottiene un account di archiviazione specificato o tutti gli account di archiviazione in un gruppo di risorse o nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ac4ab-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="ac4ab-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac4ab-109">EXAMPLES</span></span>

### <span data-ttu-id="ac4ab-110">Esempio 1: ottenere un account di archiviazione specificato</span><span class="sxs-lookup"><span data-stu-id="ac4ab-110">Example 1: Get a specified storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="ac4ab-111">Questo comando ottiene l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="ac4ab-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="ac4ab-112">Esempio 2: ottenere tutti gli account di archiviazione in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ac4ab-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="ac4ab-113">Questo comando consente di ottenere tutti gli account di archiviazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac4ab-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="ac4ab-114">Esempio 3: ottenere tutti gli account di archiviazione nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="ac4ab-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="ac4ab-115">Questo comando consente di ottenere tutti gli account di archiviazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ac4ab-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="ac4ab-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac4ab-116">PARAMETERS</span></span>

### <span data-ttu-id="ac4ab-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac4ab-117">-Name</span></span>
<span data-ttu-id="ac4ab-118">Specifica il nome dell'account di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="ac4ab-118">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac4ab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac4ab-119">-ResourceGroupName</span></span>
<span data-ttu-id="ac4ab-120">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="ac4ab-120">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac4ab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac4ab-121">-DefaultProfile</span></span>
<span data-ttu-id="ac4ab-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4ab-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac4ab-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac4ab-123">CommonParameters</span></span>
<span data-ttu-id="ac4ab-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac4ab-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac4ab-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac4ab-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac4ab-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac4ab-126">INPUTS</span></span>

## <span data-ttu-id="ac4ab-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac4ab-127">OUTPUTS</span></span>

## <span data-ttu-id="ac4ab-128">Note</span><span class="sxs-lookup"><span data-stu-id="ac4ab-128">NOTES</span></span>

## <span data-ttu-id="ac4ab-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac4ab-129">RELATED LINKS</span></span>

[<span data-ttu-id="ac4ab-130">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ac4ab-130">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="ac4ab-131">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ac4ab-131">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="ac4ab-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ac4ab-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


