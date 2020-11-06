---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 82dac83b9e252e154cedb50f7a3b90a1a78c01c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519023"
---
# <span data-ttu-id="c933f-101">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="c933f-101">Set-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="c933f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c933f-102">SYNOPSIS</span></span>
<span data-ttu-id="c933f-103">Modifica l'ottale delle autorizzazioni di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c933f-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c933f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c933f-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Permission] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c933f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c933f-105">DESCRIPTION</span></span>
<span data-ttu-id="c933f-106">Il cmdlet **set-AzureRmDataLakeStoreItemPermission** modifica l'ottale delle autorizzazioni di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c933f-106">The **Set-AzureRmDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c933f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c933f-107">EXAMPLES</span></span>

### <span data-ttu-id="c933f-108">Esempio 1: impostare l'ottale delle autorizzazioni per un elemento</span><span class="sxs-lookup"><span data-stu-id="c933f-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="c933f-109">Questo comando imposta l'ottale delle autorizzazioni per un file in 0770, che si traduce in cancellazione del bit sticky, impostando le autorizzazioni di lettura/scrittura/esecuzione per il proprietario del file, impostando le autorizzazioni di lettura/scrittura/esecuzione per il gruppo proprietario del file e deselezionando le autorizzazioni di lettura/scrittura/esecuzione per altri.</span><span class="sxs-lookup"><span data-stu-id="c933f-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="c933f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c933f-110">PARAMETERS</span></span>

### <span data-ttu-id="c933f-111">-Account</span><span class="sxs-lookup"><span data-stu-id="c933f-111">-Account</span></span>
<span data-ttu-id="c933f-112">Specifica il nome dell'account Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="c933f-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c933f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c933f-113">-DefaultProfile</span></span>
<span data-ttu-id="c933f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c933f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c933f-115">-Path</span><span class="sxs-lookup"><span data-stu-id="c933f-115">-Path</span></span>
<span data-ttu-id="c933f-116">Specifica il percorso di data Lake Store del file o della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="c933f-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c933f-117">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="c933f-117">-Permission</span></span>
<span data-ttu-id="c933f-118">Le autorizzazioni da impostare per il file o la cartella, espresse come ottale (ad esempio, "777")</span><span class="sxs-lookup"><span data-stu-id="c933f-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c933f-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c933f-119">-Confirm</span></span>
<span data-ttu-id="c933f-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c933f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c933f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c933f-121">-WhatIf</span></span>
<span data-ttu-id="c933f-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c933f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c933f-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c933f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c933f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c933f-124">CommonParameters</span></span>
<span data-ttu-id="c933f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c933f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c933f-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c933f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c933f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c933f-127">INPUTS</span></span>

### <span data-ttu-id="c933f-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c933f-128">None</span></span>
<span data-ttu-id="c933f-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c933f-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c933f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c933f-130">OUTPUTS</span></span>

### <span data-ttu-id="c933f-131">bool</span><span class="sxs-lookup"><span data-stu-id="c933f-131">bool</span></span>
<span data-ttu-id="c933f-132">Restituisce vero quando l'aggiornamento dell'autorizzazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="c933f-132">Returns true upon successfully updating the permission.</span></span>

## <span data-ttu-id="c933f-133">Note</span><span class="sxs-lookup"><span data-stu-id="c933f-133">NOTES</span></span>
* <span data-ttu-id="c933f-134">Alias: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="c933f-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="c933f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c933f-135">RELATED LINKS</span></span>

[<span data-ttu-id="c933f-136">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="c933f-136">Get-AzureRmDataLakeStoreItemPermission</span></span>](./Get-AzureRmDataLakeStoreItemPermission.md)


