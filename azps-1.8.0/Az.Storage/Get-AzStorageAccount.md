---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ba81e987e19d6698c8ea1d9e489d353d58007aea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676644"
---
# <span data-ttu-id="6b922-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6b922-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="6b922-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b922-102">SYNOPSIS</span></span>
<span data-ttu-id="6b922-103">Ottiene un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6b922-103">Gets a Storage account.</span></span>

## <span data-ttu-id="6b922-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b922-104">SYNTAX</span></span>

### <span data-ttu-id="6b922-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b922-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b922-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b922-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b922-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b922-107">DESCRIPTION</span></span>
<span data-ttu-id="6b922-108">Il cmdlet **Get-AzStorageAccount** ottiene un account di archiviazione specificato o tutti gli account di archiviazione in un gruppo di risorse o nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6b922-108">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="6b922-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b922-109">EXAMPLES</span></span>

### <span data-ttu-id="6b922-110">Esempio 1: ottenere un account di archiviazione specificato</span><span class="sxs-lookup"><span data-stu-id="6b922-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="6b922-111">Questo comando ottiene l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="6b922-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="6b922-112">Esempio 2: ottenere tutti gli account di archiviazione in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6b922-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="6b922-113">Questo comando consente di ottenere tutti gli account di archiviazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6b922-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="6b922-114">Esempio 3: ottenere tutti gli account di archiviazione nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="6b922-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="6b922-115">Questo comando consente di ottenere tutti gli account di archiviazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6b922-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="6b922-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b922-116">PARAMETERS</span></span>

### <span data-ttu-id="6b922-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b922-117">-DefaultProfile</span></span>
<span data-ttu-id="6b922-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b922-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b922-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b922-119">-Name</span></span>
<span data-ttu-id="6b922-120">Specifica il nome dell'account di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="6b922-120">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="6b922-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b922-121">-ResourceGroupName</span></span>
<span data-ttu-id="6b922-122">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="6b922-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="6b922-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b922-123">CommonParameters</span></span>
<span data-ttu-id="6b922-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b922-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b922-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b922-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b922-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b922-126">INPUTS</span></span>

### <span data-ttu-id="6b922-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6b922-127">System.String</span></span>

## <span data-ttu-id="6b922-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b922-128">OUTPUTS</span></span>

### <span data-ttu-id="6b922-129">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6b922-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="6b922-130">Note</span><span class="sxs-lookup"><span data-stu-id="6b922-130">NOTES</span></span>

## <span data-ttu-id="6b922-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b922-131">RELATED LINKS</span></span>

[<span data-ttu-id="6b922-132">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6b922-132">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="6b922-133">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6b922-133">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="6b922-134">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6b922-134">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


