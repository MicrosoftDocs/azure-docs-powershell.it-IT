---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: bf63046ebe8b73f97a80e1465060b6265f99923e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685550"
---
# <span data-ttu-id="83245-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="83245-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="83245-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83245-102">SYNOPSIS</span></span>
<span data-ttu-id="83245-103">Ottiene un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="83245-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83245-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83245-104">SYNTAX</span></span>

### <span data-ttu-id="83245-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="83245-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83245-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="83245-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83245-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83245-107">DESCRIPTION</span></span>
<span data-ttu-id="83245-108">Il cmdlet **Get-AzureRmStorageAccount** ottiene un account di archiviazione specificato o tutti gli account di archiviazione in un gruppo di risorse o nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="83245-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="83245-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83245-109">EXAMPLES</span></span>

### <span data-ttu-id="83245-110">Esempio 1: ottenere un account di archiviazione specificato</span><span class="sxs-lookup"><span data-stu-id="83245-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="83245-111">Questo comando ottiene l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="83245-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="83245-112">Esempio 2: ottenere tutti gli account di archiviazione in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="83245-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="83245-113">Questo comando consente di ottenere tutti gli account di archiviazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="83245-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="83245-114">Esempio 3: ottenere tutti gli account di archiviazione nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="83245-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="83245-115">Questo comando consente di ottenere tutti gli account di archiviazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="83245-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="83245-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83245-116">PARAMETERS</span></span>

### <span data-ttu-id="83245-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83245-117">-DefaultProfile</span></span>
<span data-ttu-id="83245-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83245-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83245-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="83245-119">-Name</span></span>
<span data-ttu-id="83245-120">Specifica il nome dell'account di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="83245-120">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="83245-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83245-121">-ResourceGroupName</span></span>
<span data-ttu-id="83245-122">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="83245-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="83245-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83245-123">CommonParameters</span></span>
<span data-ttu-id="83245-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83245-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83245-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83245-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83245-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83245-126">INPUTS</span></span>

### <span data-ttu-id="83245-127">System. String</span><span class="sxs-lookup"><span data-stu-id="83245-127">System.String</span></span>

## <span data-ttu-id="83245-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83245-128">OUTPUTS</span></span>

### <span data-ttu-id="83245-129">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="83245-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="83245-130">Note</span><span class="sxs-lookup"><span data-stu-id="83245-130">NOTES</span></span>

## <span data-ttu-id="83245-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83245-131">RELATED LINKS</span></span>

[<span data-ttu-id="83245-132">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="83245-132">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="83245-133">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="83245-133">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="83245-134">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="83245-134">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


