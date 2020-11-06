---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Sync-AzureRmMediaServiceStorageKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Sync-AzureRmMediaServiceStorageKeys.md
ms.openlocfilehash: 71112bf54f4de8e0c7e4fd1ecfd296eff45ac868
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520506"
---
# <span data-ttu-id="e6bef-101">Sync-AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="e6bef-101">Sync-AzureRmMediaServiceStorageKeys</span></span>

## <span data-ttu-id="e6bef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6bef-102">SYNOPSIS</span></span>
<span data-ttu-id="e6bef-103">Sincronizza le chiavi dell'account di archiviazione per un account di archiviazione associato al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="e6bef-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6bef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6bef-104">SYNTAX</span></span>

```
Sync-AzureRmMediaServiceStorageKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6bef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6bef-105">DESCRIPTION</span></span>
<span data-ttu-id="e6bef-106">Il cmdlet **Sync-AzureRmMediaServiceStorageKeys** sincronizza le chiavi dell'account di archiviazione per un account di archiviazione associato al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="e6bef-106">The **Sync-AzureRmMediaServiceStorageKeys** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="e6bef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6bef-107">EXAMPLES</span></span>

### <span data-ttu-id="e6bef-108">Esempio 1: sincronizzare le chiavi dell'account di archiviazione per un account di archiviazione associato al servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="e6bef-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzureRmStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzureRmMediaServiceStorageKeys -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="e6bef-109">Il primo comando usa il cmdlet Get-AzureRmStorageAccount per ottenere l'account di archiviazione denominato Storage135 che appartiene a ResourceGroup001 e archivia il risultato nella variabile denominata $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="e6bef-109">The first command uses the Get-AzureRmStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>

<span data-ttu-id="e6bef-110">Il secondo comando Sincronizza le chiavi dell'account di archiviazione per il servizio multimediale denominato MediaService001 usando la proprietà **ID** contenuta nella variabile $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="e6bef-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="e6bef-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6bef-111">PARAMETERS</span></span>

### <span data-ttu-id="e6bef-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e6bef-112">-AccountName</span></span>
<span data-ttu-id="e6bef-113">Specifica il nome del servizio multimediale sincronizzato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6bef-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6bef-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6bef-114">-ResourceGroupName</span></span>
<span data-ttu-id="e6bef-115">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="e6bef-115">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="e6bef-116">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e6bef-116">-StorageAccountId</span></span>
<span data-ttu-id="e6bef-117">Specifica l'ID account di archiviazione associato all'account del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="e6bef-117">Specifies the storage account ID associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6bef-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e6bef-118">-Confirm</span></span>
<span data-ttu-id="e6bef-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6bef-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6bef-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6bef-120">-WhatIf</span></span>
<span data-ttu-id="e6bef-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6bef-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6bef-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6bef-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6bef-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6bef-123">-DefaultProfile</span></span>
<span data-ttu-id="e6bef-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6bef-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6bef-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6bef-125">CommonParameters</span></span>
<span data-ttu-id="e6bef-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6bef-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6bef-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6bef-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6bef-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6bef-128">INPUTS</span></span>

## <span data-ttu-id="e6bef-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6bef-129">OUTPUTS</span></span>

### <span data-ttu-id="e6bef-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6bef-130">System.Boolean</span></span>

## <span data-ttu-id="e6bef-131">Note</span><span class="sxs-lookup"><span data-stu-id="e6bef-131">NOTES</span></span>

## <span data-ttu-id="e6bef-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6bef-132">RELATED LINKS</span></span>

