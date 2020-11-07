---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/new-azurermmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
ms.openlocfilehash: 7296d744749dd037c10d0d4d5ee2b0461a55b794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686502"
---
# <span data-ttu-id="dcafd-101">New-AzureRmMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="dcafd-101">New-AzureRmMediaServiceStorageConfig</span></span>

## <span data-ttu-id="dcafd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dcafd-102">SYNOPSIS</span></span>
<span data-ttu-id="dcafd-103">Creare una configurazione dell'account di archiviazione per i cmdlet del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="dcafd-103">Create a storage account configuration for the media service cmdlets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcafd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dcafd-104">SYNTAX</span></span>

```
New-AzureRmMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcafd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dcafd-105">DESCRIPTION</span></span>
<span data-ttu-id="dcafd-106">Il cmdlet **New-AzureRmMediaServiceStorageConfig** crea una configurazione dell'account di archiviazione per i cmdlet del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="dcafd-106">The **New-AzureRmMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="dcafd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dcafd-107">EXAMPLES</span></span>

### <span data-ttu-id="dcafd-108">Esempio 1: creare una configurazione dell'account di archiviazione per i cmdlet del servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="dcafd-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="dcafd-109">Il primo comando crea un oggetto account di archiviazione usando **il cmdlet New-AzureRmStorageAccount** .</span><span class="sxs-lookup"><span data-stu-id="dcafd-109">The first command creates a storage account object by using **the New-AzureRmStorageAccount** cmdlet.</span></span>
<span data-ttu-id="dcafd-110">Il comando chiama questo account di archiviazione storage1 e il tipo è denominato Standard_GRS e archivia il risultato nella variabile denominata $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="dcafd-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>

<span data-ttu-id="dcafd-111">Il secondo comando crea un oggetto di configurazione dello spazio di archiviazione come account di archiviazione principale associato al servizio multimediale utilizzando le informazioni sull'ID account di archiviazione archiviate nella variabile $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="dcafd-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="dcafd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dcafd-112">PARAMETERS</span></span>

### <span data-ttu-id="dcafd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcafd-113">-DefaultProfile</span></span>
<span data-ttu-id="dcafd-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="dcafd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcafd-115">-Inprimary</span><span class="sxs-lookup"><span data-stu-id="dcafd-115">-IsPrimary</span></span>
<span data-ttu-id="dcafd-116">Indica che il cmdlet crea l'account di archiviazione come spazio di archiviazione principale per il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="dcafd-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcafd-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="dcafd-117">-StorageAccountId</span></span>
<span data-ttu-id="dcafd-118">Specifica l'ID dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="dcafd-118">Specifies the ID of the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcafd-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dcafd-119">-Confirm</span></span>
<span data-ttu-id="dcafd-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcafd-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcafd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcafd-121">-WhatIf</span></span>
<span data-ttu-id="dcafd-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dcafd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcafd-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dcafd-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcafd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcafd-124">CommonParameters</span></span>
<span data-ttu-id="dcafd-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcafd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcafd-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcafd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcafd-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dcafd-127">INPUTS</span></span>

### <span data-ttu-id="dcafd-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="dcafd-128">None</span></span>
<span data-ttu-id="dcafd-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="dcafd-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dcafd-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dcafd-130">OUTPUTS</span></span>

### <span data-ttu-id="dcafd-131">Microsoft. Azure. Commands. Media. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcafd-131">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="dcafd-132">Note</span><span class="sxs-lookup"><span data-stu-id="dcafd-132">NOTES</span></span>

## <span data-ttu-id="dcafd-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dcafd-133">RELATED LINKS</span></span>

[<span data-ttu-id="dcafd-134">Sincronizzazione-AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="dcafd-134">Sync-AzureRmMediaServiceStorageKeys</span></span>](./Sync-AzureRmMediaServiceStorageKeys.md)


