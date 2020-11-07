---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
ms.openlocfilehash: 73680e82a9d898075e905d88bcc8602609a5612d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686135"
---
# <span data-ttu-id="ea142-101">Set-AzureRmCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ea142-101">Set-AzureRmCurrentStorageAccount</span></span>

## <span data-ttu-id="ea142-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea142-102">SYNOPSIS</span></span>
<span data-ttu-id="ea142-103">Modifica l'account di archiviazione corrente dell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="ea142-103">Modifies the current Storage account of the specified subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea142-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea142-104">SYNTAX</span></span>

### <span data-ttu-id="ea142-105">UsingResourceGroupAndNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ea142-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzureRmCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea142-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="ea142-106">UsingStorageContext</span></span>
```
Set-AzureRmCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea142-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea142-107">DESCRIPTION</span></span>
<span data-ttu-id="ea142-108">Il cmdlet **set-AzureRmCurrentStorageAccount** modifica l'account di archiviazione di Azure corrente dell'abbonamento Azure specificato in Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ea142-108">The **Set-AzureRmCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="ea142-109">L'account di archiviazione corrente viene usato come predefinito quando si accede allo spazio di archiviazione senza specificare un nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ea142-109">The current storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="ea142-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea142-110">EXAMPLES</span></span>

### <span data-ttu-id="ea142-111">Esempio 1: impostare l'account di archiviazione corrente</span><span class="sxs-lookup"><span data-stu-id="ea142-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzureRmCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="ea142-112">Questo comando imposta l'account di archiviazione predefinito per l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="ea142-112">This command sets the default storage account for the specified subscription.</span></span>

## <span data-ttu-id="ea142-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea142-113">PARAMETERS</span></span>

### <span data-ttu-id="ea142-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ea142-114">-Context</span></span>
<span data-ttu-id="ea142-115">Specifica un oggetto **AzureStorageContext** per l'account di archiviazione corrente.</span><span class="sxs-lookup"><span data-stu-id="ea142-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="ea142-116">Per ottenere un oggetto di contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ea142-116">To obtain a storage context object, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UsingStorageContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea142-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea142-117">-Name</span></span>
<span data-ttu-id="ea142-118">Specifica il nome dell'account di archiviazione modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea142-118">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea142-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea142-119">-ResourceGroupName</span></span>
<span data-ttu-id="ea142-120">Specifica il gruppo di risorse che contiene l'account di archiviazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="ea142-120">Specifies the resource group that contains the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea142-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea142-121">-DefaultProfile</span></span>
<span data-ttu-id="ea142-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea142-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea142-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea142-123">CommonParameters</span></span>
<span data-ttu-id="ea142-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea142-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea142-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea142-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea142-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea142-126">INPUTS</span></span>

## <span data-ttu-id="ea142-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea142-127">OUTPUTS</span></span>

## <span data-ttu-id="ea142-128">Note</span><span class="sxs-lookup"><span data-stu-id="ea142-128">NOTES</span></span>

## <span data-ttu-id="ea142-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea142-129">RELATED LINKS</span></span>

[<span data-ttu-id="ea142-130">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ea142-130">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


