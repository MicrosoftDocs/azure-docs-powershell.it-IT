---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 72D332BA-A30B-45B9-875C-DF9D33299E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ddfbdc7da2f398ae1db11cf87de344c4f4ed5de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023636"
---
# <span data-ttu-id="1d416-101">Export-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="1d416-101">Export-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="1d416-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d416-102">SYNOPSIS</span></span>
<span data-ttu-id="1d416-103">Esporta tutti i dischi utente da una raccolta RemoteApp di Azure nell'account di archiviazione di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="1d416-103">Exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="1d416-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d416-104">SYNTAX</span></span>

```
Export-AzureRemoteAppUserDisk [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d416-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d416-105">DESCRIPTION</span></span>
<span data-ttu-id="1d416-106">Il cmdlet **Export-AzureRemoteAppUserDisk** Esporta tutti i dischi utente da una raccolta RemoteApp di Azure nell'account di archiviazione di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="1d416-106">The **Export-AzureRemoteAppUserDisk** cmdlet exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="1d416-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d416-107">EXAMPLES</span></span>

### <span data-ttu-id="1d416-108">Esempio 1: esportare tutti i dischi utente da una raccolta nell'account di archiviazione di Azure specificato</span><span class="sxs-lookup"><span data-stu-id="1d416-108">Example 1: Export all the user disks from a collection to the specified Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppUserDisk -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingUserDisk
```

<span data-ttu-id="1d416-109">Questo comando Esporta tutti i dischi utente dalla raccolta denominata Contoso in un contenitore denominato ContainerName nell'account di archiviazione di Azure specificato con nome AccountName e Key AccountKey.</span><span class="sxs-lookup"><span data-stu-id="1d416-109">This command exports all the user disks from the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="1d416-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d416-110">PARAMETERS</span></span>

### <span data-ttu-id="1d416-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="1d416-111">-CollectionName</span></span>
<span data-ttu-id="1d416-112">Specifica il nome della raccolta RemoteApp di Azure di origine.</span><span class="sxs-lookup"><span data-stu-id="1d416-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d416-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="1d416-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="1d416-114">Specifica il nome di un contenitore nell'account di archiviazione di Azure di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1d416-114">Specifies the name of a container in the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d416-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1d416-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="1d416-116">Specifica la chiave dell'account di archiviazione di Azure di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1d416-116">Specifies the Key of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d416-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1d416-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="1d416-118">Specifica il nome dell'account di archiviazione di Azure di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1d416-118">Specifies the name of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d416-119">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="1d416-119">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="1d416-120">Indica che il cmdlet sovrascrive il disco utente esistente.</span><span class="sxs-lookup"><span data-stu-id="1d416-120">Indicates that the cmdlet overwrites the existing user disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d416-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="1d416-121">-Profile</span></span>
<span data-ttu-id="1d416-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d416-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1d416-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1d416-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d416-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1d416-124">-Confirm</span></span>
<span data-ttu-id="1d416-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d416-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d416-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d416-126">-WhatIf</span></span>
<span data-ttu-id="1d416-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d416-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d416-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d416-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d416-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d416-129">CommonParameters</span></span>
<span data-ttu-id="1d416-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d416-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d416-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d416-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d416-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d416-132">INPUTS</span></span>

## <span data-ttu-id="1d416-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d416-133">OUTPUTS</span></span>

## <span data-ttu-id="1d416-134">Note</span><span class="sxs-lookup"><span data-stu-id="1d416-134">NOTES</span></span>

## <span data-ttu-id="1d416-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d416-135">RELATED LINKS</span></span>

[<span data-ttu-id="1d416-136">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="1d416-136">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)

[<span data-ttu-id="1d416-137">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="1d416-137">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


