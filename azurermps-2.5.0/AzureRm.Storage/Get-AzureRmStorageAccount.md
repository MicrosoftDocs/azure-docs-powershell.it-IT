---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: dafceede3c3732af423052d33ba125c4ad292d20
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866188"
---
# <span data-ttu-id="0bd4e-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0bd4e-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="0bd4e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0bd4e-102">SYNOPSIS</span></span>
<span data-ttu-id="0bd4e-103">Ottiene un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0bd4e-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bd4e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0bd4e-104">SYNTAX</span></span>

### <span data-ttu-id="0bd4e-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bd4e-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0bd4e-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bd4e-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bd4e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bd4e-107">DESCRIPTION</span></span>
<span data-ttu-id="0bd4e-108">Il cmdlet **Get-AzureRmStorageAccount** ottiene un account di archiviazione specificato o tutti gli account di archiviazione in un gruppo di risorse o nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0bd4e-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="0bd4e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0bd4e-109">EXAMPLES</span></span>

### <span data-ttu-id="0bd4e-110">Esempio 1: ottenere un account di archiviazione specificato</span><span class="sxs-lookup"><span data-stu-id="0bd4e-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="0bd4e-111">Questo comando ottiene l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="0bd4e-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="0bd4e-112">Esempio 2: ottenere tutti gli account di archiviazione in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0bd4e-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="0bd4e-113">Questo comando consente di ottenere tutti gli account di archiviazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0bd4e-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="0bd4e-114">Esempio 3: ottenere tutti gli account di archiviazione nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="0bd4e-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="0bd4e-115">Questo comando consente di ottenere tutti gli account di archiviazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0bd4e-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="0bd4e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0bd4e-116">PARAMETERS</span></span>

### <span data-ttu-id="0bd4e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bd4e-117">-DefaultProfile</span></span>
<span data-ttu-id="0bd4e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0bd4e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bd4e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0bd4e-119">-Name</span></span>
<span data-ttu-id="0bd4e-120">Specifica il nome dell'account di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="0bd4e-120">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="0bd4e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bd4e-121">-ResourceGroupName</span></span>
<span data-ttu-id="0bd4e-122">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="0bd4e-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="0bd4e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bd4e-123">CommonParameters</span></span>
<span data-ttu-id="0bd4e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bd4e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bd4e-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bd4e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bd4e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0bd4e-126">INPUTS</span></span>

### <span data-ttu-id="0bd4e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0bd4e-127">System.String</span></span>

## <span data-ttu-id="0bd4e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bd4e-128">OUTPUTS</span></span>

### <span data-ttu-id="0bd4e-129">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0bd4e-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="0bd4e-130">Note</span><span class="sxs-lookup"><span data-stu-id="0bd4e-130">NOTES</span></span>

## <span data-ttu-id="0bd4e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0bd4e-131">RELATED LINKS</span></span>

[<span data-ttu-id="0bd4e-132">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0bd4e-132">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="0bd4e-133">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0bd4e-133">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="0bd4e-134">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0bd4e-134">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


