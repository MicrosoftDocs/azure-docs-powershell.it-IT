---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 9a0b5f54b4bdbdee80cdade05716ff5508324b91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685948"
---
# <span data-ttu-id="1fcb1-101">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="1fcb1-101">Set-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="1fcb1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1fcb1-102">SYNOPSIS</span></span>
<span data-ttu-id="1fcb1-103">Modifica l'ottale delle autorizzazioni di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fcb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1fcb1-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Permission] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fcb1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fcb1-105">DESCRIPTION</span></span>
<span data-ttu-id="1fcb1-106">Il cmdlet **set-AzureRmDataLakeStoreItemPermission** modifica l'ottale delle autorizzazioni di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-106">The **Set-AzureRmDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1fcb1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1fcb1-107">EXAMPLES</span></span>

### <span data-ttu-id="1fcb1-108">Esempio 1: impostare l'ottale delle autorizzazioni per un elemento</span><span class="sxs-lookup"><span data-stu-id="1fcb1-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="1fcb1-109">Questo comando imposta l'ottale delle autorizzazioni per un file in 0770, che si traduce in cancellazione del bit sticky, impostando le autorizzazioni di lettura/scrittura/esecuzione per il proprietario del file, impostando le autorizzazioni di lettura/scrittura/esecuzione per il gruppo proprietario del file e deselezionando le autorizzazioni di lettura/scrittura/esecuzione per altri.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="1fcb1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1fcb1-110">PARAMETERS</span></span>

### <span data-ttu-id="1fcb1-111">-Account</span><span class="sxs-lookup"><span data-stu-id="1fcb1-111">-Account</span></span>
<span data-ttu-id="1fcb1-112">Specifica il nome dell'account Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fcb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fcb1-113">-DefaultProfile</span></span>
<span data-ttu-id="1fcb1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fcb1-115">-Path</span><span class="sxs-lookup"><span data-stu-id="1fcb1-115">-Path</span></span>
<span data-ttu-id="1fcb1-116">Specifica il percorso di data Lake Store del file o della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="1fcb1-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fcb1-117">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="1fcb1-117">-Permission</span></span>
<span data-ttu-id="1fcb1-118">Le autorizzazioni da impostare per il file o la cartella, espresse come ottale (ad esempio, "777")</span><span class="sxs-lookup"><span data-stu-id="1fcb1-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fcb1-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1fcb1-119">-Confirm</span></span>
<span data-ttu-id="1fcb1-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fcb1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fcb1-121">-WhatIf</span></span>
<span data-ttu-id="1fcb1-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fcb1-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fcb1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fcb1-124">CommonParameters</span></span>
<span data-ttu-id="1fcb1-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fcb1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fcb1-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fcb1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fcb1-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1fcb1-127">INPUTS</span></span>

### <span data-ttu-id="1fcb1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1fcb1-128">System.String</span></span>

### <span data-ttu-id="1fcb1-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1fcb1-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1fcb1-130">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1fcb1-130">System.Int32</span></span>

## <span data-ttu-id="1fcb1-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1fcb1-131">OUTPUTS</span></span>

### <span data-ttu-id="1fcb1-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1fcb1-132">System.Boolean</span></span>

## <span data-ttu-id="1fcb1-133">Note</span><span class="sxs-lookup"><span data-stu-id="1fcb1-133">NOTES</span></span>
* <span data-ttu-id="1fcb1-134">Alias: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="1fcb1-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="1fcb1-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1fcb1-135">RELATED LINKS</span></span>

[<span data-ttu-id="1fcb1-136">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="1fcb1-136">Get-AzureRmDataLakeStoreItemPermission</span></span>](./Get-AzureRmDataLakeStoreItemPermission.md)


