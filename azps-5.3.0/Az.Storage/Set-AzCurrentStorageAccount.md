---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: c57f8a7ce6b4f7275e724c777c2e6dfd54a680ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474650"
---
# <span data-ttu-id="e4d8d-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e4d8d-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="e4d8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="e4d8d-103">Modifica l'account di archiviazione corrente dell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="e4d8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4d8d-104">SYNTAX</span></span>

### <span data-ttu-id="e4d8d-105">UsingResourceGroupAndNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4d8d-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4d8d-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="e4d8d-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4d8d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4d8d-107">DESCRIPTION</span></span>
<span data-ttu-id="e4d8d-108">Il cmdlet **set-AzCurrentStorageAccount** modifica l'account di archiviazione di Azure corrente dell'abbonamento Azure specificato in Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="e4d8d-109">L'account di archiviazione corrente viene usato come predefinito quando si accede allo spazio di archiviazione senza specificare un nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="e4d8d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4d8d-110">EXAMPLES</span></span>

### <span data-ttu-id="e4d8d-111">Esempio 1: impostare l'account di archiviazione corrente</span><span class="sxs-lookup"><span data-stu-id="e4d8d-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="e4d8d-112">Questo comando imposta l'account di archiviazione predefinito per l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="e4d8d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4d8d-113">PARAMETERS</span></span>

### <span data-ttu-id="e4d8d-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e4d8d-114">-Context</span></span>
<span data-ttu-id="e4d8d-115">Specifica un oggetto **AzureStorageContext** per l'account di archiviazione corrente.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="e4d8d-116">Per ottenere un oggetto di contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e4d8d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4d8d-117">-DefaultProfile</span></span>
<span data-ttu-id="e4d8d-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4d8d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4d8d-119">-Name</span></span>
<span data-ttu-id="e4d8d-120">Specifica il nome dell'account di archiviazione modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e4d8d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4d8d-121">-ResourceGroupName</span></span>
<span data-ttu-id="e4d8d-122">Specifica il gruppo di risorse che contiene l'account di archiviazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-122">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="e4d8d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4d8d-123">CommonParameters</span></span>
<span data-ttu-id="e4d8d-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4d8d-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4d8d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4d8d-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4d8d-126">INPUTS</span></span>

### <span data-ttu-id="e4d8d-127">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e4d8d-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="e4d8d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e4d8d-128">System.String</span></span>

## <span data-ttu-id="e4d8d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4d8d-129">OUTPUTS</span></span>

### <span data-ttu-id="e4d8d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e4d8d-130">System.String</span></span>

## <span data-ttu-id="e4d8d-131">Note</span><span class="sxs-lookup"><span data-stu-id="e4d8d-131">NOTES</span></span>

## <span data-ttu-id="e4d8d-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4d8d-132">RELATED LINKS</span></span>

[<span data-ttu-id="e4d8d-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e4d8d-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


