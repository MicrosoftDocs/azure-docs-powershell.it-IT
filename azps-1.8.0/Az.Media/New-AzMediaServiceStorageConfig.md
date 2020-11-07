---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: 8fb6e4a683decc8b5615a7cf0c8088681578f8ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835183"
---
# <span data-ttu-id="69417-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="69417-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="69417-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69417-102">SYNOPSIS</span></span>
<span data-ttu-id="69417-103">Creare una configurazione dell'account di archiviazione per i cmdlet del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="69417-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="69417-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69417-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69417-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69417-105">DESCRIPTION</span></span>
<span data-ttu-id="69417-106">Il cmdlet **New-AzMediaServiceStorageConfig** crea una configurazione dell'account di archiviazione per i cmdlet del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="69417-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="69417-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69417-107">EXAMPLES</span></span>

### <span data-ttu-id="69417-108">Esempio 1: creare una configurazione dell'account di archiviazione per i cmdlet del servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="69417-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="69417-109">Il primo comando crea un oggetto account di archiviazione usando **il cmdlet New-AzStorageAccount** .</span><span class="sxs-lookup"><span data-stu-id="69417-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="69417-110">Il comando chiama questo account di archiviazione storage1 e il tipo è denominato Standard_GRS e archivia il risultato nella variabile denominata $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="69417-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="69417-111">Il secondo comando crea un oggetto di configurazione dello spazio di archiviazione come account di archiviazione principale associato al servizio multimediale utilizzando le informazioni sull'ID account di archiviazione archiviate nella variabile $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="69417-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="69417-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69417-112">PARAMETERS</span></span>

### <span data-ttu-id="69417-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69417-113">-DefaultProfile</span></span>
<span data-ttu-id="69417-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="69417-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69417-115">-Inprimary</span><span class="sxs-lookup"><span data-stu-id="69417-115">-IsPrimary</span></span>
<span data-ttu-id="69417-116">Indica che il cmdlet crea l'account di archiviazione come spazio di archiviazione principale per il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="69417-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69417-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="69417-117">-StorageAccountId</span></span>
<span data-ttu-id="69417-118">Specifica l'ID dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="69417-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="69417-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="69417-119">-Confirm</span></span>
<span data-ttu-id="69417-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69417-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69417-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69417-121">-WhatIf</span></span>
<span data-ttu-id="69417-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69417-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69417-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69417-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69417-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69417-124">CommonParameters</span></span>
<span data-ttu-id="69417-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69417-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69417-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69417-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69417-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69417-127">INPUTS</span></span>

### <span data-ttu-id="69417-128">System. String</span><span class="sxs-lookup"><span data-stu-id="69417-128">System.String</span></span>

## <span data-ttu-id="69417-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69417-129">OUTPUTS</span></span>

### <span data-ttu-id="69417-130">Microsoft. Azure. Commands. Media. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="69417-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="69417-131">Note</span><span class="sxs-lookup"><span data-stu-id="69417-131">NOTES</span></span>

## <span data-ttu-id="69417-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69417-132">RELATED LINKS</span></span>

[<span data-ttu-id="69417-133">Sincronizzazione-AzMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="69417-133">Sync-AzMediaServiceStorageKeys</span></span>](./Sync-AzMediaServiceStorageKeys.md)


