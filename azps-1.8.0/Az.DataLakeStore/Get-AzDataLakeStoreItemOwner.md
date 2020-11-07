---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: 64af120d793719d4bcd6a24cc3d480cc8f6c104f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684532"
---
# <span data-ttu-id="0d808-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="0d808-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="0d808-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d808-102">SYNOPSIS</span></span>
<span data-ttu-id="0d808-103">Ottiene il proprietario di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d808-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0d808-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d808-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d808-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d808-105">DESCRIPTION</span></span>
<span data-ttu-id="0d808-106">Il cmdlet **Get-AzDataLakeStoreItemOwner** ottiene il proprietario di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d808-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0d808-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d808-107">EXAMPLES</span></span>

### <span data-ttu-id="0d808-108">Esempio 1: ottenere il proprietario per una directory</span><span class="sxs-lookup"><span data-stu-id="0d808-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="0d808-109">Questo comando consente di ottenere il proprietario dell'utente per la directory radice dell'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="0d808-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="0d808-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d808-110">PARAMETERS</span></span>

### <span data-ttu-id="0d808-111">-Account</span><span class="sxs-lookup"><span data-stu-id="0d808-111">-Account</span></span>
<span data-ttu-id="0d808-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d808-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0d808-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d808-113">-DefaultProfile</span></span>
<span data-ttu-id="0d808-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d808-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d808-115">-Path</span><span class="sxs-lookup"><span data-stu-id="0d808-115">-Path</span></span>
<span data-ttu-id="0d808-116">Specifica il percorso di data Lake Store di un elemento, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="0d808-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0d808-117">-Digitare</span><span class="sxs-lookup"><span data-stu-id="0d808-117">-Type</span></span>
<span data-ttu-id="0d808-118">Specifica il tipo di proprietario da ottenere.</span><span class="sxs-lookup"><span data-stu-id="0d808-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="0d808-119">I valori accettabili per questo parametro sono: utente e gruppo.</span><span class="sxs-lookup"><span data-stu-id="0d808-119">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d808-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d808-120">CommonParameters</span></span>
<span data-ttu-id="0d808-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d808-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d808-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d808-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d808-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d808-123">INPUTS</span></span>

### <span data-ttu-id="0d808-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0d808-124">System.String</span></span>

### <span data-ttu-id="0d808-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0d808-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="0d808-126">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="0d808-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="0d808-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d808-127">OUTPUTS</span></span>

### <span data-ttu-id="0d808-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0d808-128">System.String</span></span>

## <span data-ttu-id="0d808-129">Note</span><span class="sxs-lookup"><span data-stu-id="0d808-129">NOTES</span></span>

## <span data-ttu-id="0d808-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d808-130">RELATED LINKS</span></span>

[<span data-ttu-id="0d808-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="0d808-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


