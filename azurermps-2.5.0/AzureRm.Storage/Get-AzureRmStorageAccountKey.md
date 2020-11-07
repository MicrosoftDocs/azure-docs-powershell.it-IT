---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountkey
schema: 2.0.0
ms.openlocfilehash: 365664e10e5c173881d014df5def1bb593d743bd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866189"
---
# <span data-ttu-id="e6a3d-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e6a3d-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="e6a3d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6a3d-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a3d-103">Ottiene i tasti di scelta per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a3d-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6a3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6a3d-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6a3d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6a3d-105">DESCRIPTION</span></span>
<span data-ttu-id="e6a3d-106">Il cmdlet **Get-AzureRmStorageAccountKey** ottiene i tasti di scelta per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a3d-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="e6a3d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6a3d-107">EXAMPLES</span></span>

### <span data-ttu-id="e6a3d-108">Esempio 1: ottenere i tasti di scelta per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e6a3d-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="e6a3d-109">Questo comando consente di ottenere le chiavi per l'account di archiviazione di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="e6a3d-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="e6a3d-110">Esempio 2: ottenere un tasto di accesso specifico per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e6a3d-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

## <span data-ttu-id="e6a3d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6a3d-111">PARAMETERS</span></span>

### <span data-ttu-id="e6a3d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a3d-112">-DefaultProfile</span></span>
<span data-ttu-id="e6a3d-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a3d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6a3d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6a3d-114">-Name</span></span>
<span data-ttu-id="e6a3d-115">Specifica il nome dell'account di archiviazione per cui questo cmdlet ottiene le chiavi.</span><span class="sxs-lookup"><span data-stu-id="e6a3d-115">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="e6a3d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6a3d-116">-ResourceGroupName</span></span>
<span data-ttu-id="e6a3d-117">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e6a3d-117">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="e6a3d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a3d-118">CommonParameters</span></span>
<span data-ttu-id="e6a3d-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6a3d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a3d-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6a3d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a3d-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6a3d-121">INPUTS</span></span>

### <span data-ttu-id="e6a3d-122">System. String</span><span class="sxs-lookup"><span data-stu-id="e6a3d-122">System.String</span></span>

## <span data-ttu-id="e6a3d-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6a3d-123">OUTPUTS</span></span>

### <span data-ttu-id="e6a3d-124">Microsoft. Azure. Management. storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e6a3d-124">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="e6a3d-125">Note</span><span class="sxs-lookup"><span data-stu-id="e6a3d-125">NOTES</span></span>

## <span data-ttu-id="e6a3d-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6a3d-126">RELATED LINKS</span></span>

[<span data-ttu-id="e6a3d-127">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e6a3d-127">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)


