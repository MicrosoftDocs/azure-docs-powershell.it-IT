---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: 4f929c720859df529dbf2954da9ddb51eedec8b4
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409291"
---
# <span data-ttu-id="cabd9-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="cabd9-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="cabd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cabd9-102">SYNOPSIS</span></span>
<span data-ttu-id="cabd9-103">Creare una configurazione dell'account di archiviazione per i cmdlet del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="cabd9-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="cabd9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cabd9-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cabd9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cabd9-105">DESCRIPTION</span></span>
<span data-ttu-id="cabd9-106">Il cmdlet **New-AzMediaServiceStorageConfig crea** una configurazione dell'account di archiviazione per i cmdlet del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="cabd9-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="cabd9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cabd9-107">EXAMPLES</span></span>

### <span data-ttu-id="cabd9-108">Esempio 1: Creare una configurazione di account di archiviazione per i cmdlet del servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="cabd9-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="cabd9-109">Il primo comando crea un oggetto account di archiviazione usando il cmdlet **New-AzStorageAccount.**</span><span class="sxs-lookup"><span data-stu-id="cabd9-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="cabd9-110">Il comando chiama questo account di archiviazione Storage1 e il tipo è denominato Standard_GRS e archivia il risultato nella variabile $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="cabd9-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="cabd9-111">Il secondo comando crea un oggetto configurazione di archiviazione come account di archiviazione principale associato al servizio multimediale usando le informazioni sull'ID dell'account di archiviazione archiviate nella variabile $StorageAccount archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cabd9-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="cabd9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cabd9-112">PARAMETERS</span></span>

### <span data-ttu-id="cabd9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cabd9-113">-DefaultProfile</span></span>
<span data-ttu-id="cabd9-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cabd9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cabd9-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="cabd9-115">-IsPrimary</span></span>
<span data-ttu-id="cabd9-116">Indica che il cmdlet crea l'account di archiviazione come archivio principale per il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="cabd9-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

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

### <span data-ttu-id="cabd9-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cabd9-117">-StorageAccountId</span></span>
<span data-ttu-id="cabd9-118">Specifica l'ID dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cabd9-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="cabd9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cabd9-119">-Confirm</span></span>
<span data-ttu-id="cabd9-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cabd9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cabd9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cabd9-121">-WhatIf</span></span>
<span data-ttu-id="cabd9-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cabd9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cabd9-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cabd9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cabd9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cabd9-124">CommonParameters</span></span>
<span data-ttu-id="cabd9-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cabd9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cabd9-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cabd9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cabd9-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="cabd9-127">INPUTS</span></span>

### <span data-ttu-id="cabd9-128">System.String</span><span class="sxs-lookup"><span data-stu-id="cabd9-128">System.String</span></span>

## <span data-ttu-id="cabd9-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cabd9-129">OUTPUTS</span></span>

### <span data-ttu-id="cabd9-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cabd9-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="cabd9-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="cabd9-131">NOTES</span></span>

## <span data-ttu-id="cabd9-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cabd9-132">RELATED LINKS</span></span>



