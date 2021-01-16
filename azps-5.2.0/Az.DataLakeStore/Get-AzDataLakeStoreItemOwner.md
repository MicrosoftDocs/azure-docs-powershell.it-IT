---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: ae87c0cc6c9ccea3935e3bd0856d033895070515
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343900"
---
# <span data-ttu-id="6a32f-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="6a32f-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="6a32f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a32f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a32f-103">Ottiene il proprietario di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6a32f-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6a32f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a32f-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a32f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a32f-105">DESCRIPTION</span></span>
<span data-ttu-id="6a32f-106">Il cmdlet **Get-AzDataLakeStoreItemOwner** ottiene il proprietario di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6a32f-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6a32f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a32f-107">EXAMPLES</span></span>

### <span data-ttu-id="6a32f-108">Esempio 1: ottenere il proprietario per una directory</span><span class="sxs-lookup"><span data-stu-id="6a32f-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="6a32f-109">Questo comando consente di ottenere il proprietario dell'utente per la directory radice dell'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="6a32f-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="6a32f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a32f-110">PARAMETERS</span></span>

### <span data-ttu-id="6a32f-111">-Account</span><span class="sxs-lookup"><span data-stu-id="6a32f-111">-Account</span></span>
<span data-ttu-id="6a32f-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6a32f-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6a32f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a32f-113">-DefaultProfile</span></span>
<span data-ttu-id="6a32f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a32f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a32f-115">-Path</span><span class="sxs-lookup"><span data-stu-id="6a32f-115">-Path</span></span>
<span data-ttu-id="6a32f-116">Specifica il percorso di data Lake Store di un elemento, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="6a32f-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6a32f-117">-Digitare</span><span class="sxs-lookup"><span data-stu-id="6a32f-117">-Type</span></span>
<span data-ttu-id="6a32f-118">Specifica il tipo di proprietario da ottenere.</span><span class="sxs-lookup"><span data-stu-id="6a32f-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="6a32f-119">I valori accettabili per questo parametro sono: utente e gruppo.</span><span class="sxs-lookup"><span data-stu-id="6a32f-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="6a32f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a32f-120">CommonParameters</span></span>
<span data-ttu-id="6a32f-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a32f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a32f-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a32f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a32f-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a32f-123">INPUTS</span></span>

### <span data-ttu-id="6a32f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6a32f-124">System.String</span></span>

### <span data-ttu-id="6a32f-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="6a32f-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6a32f-126">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="6a32f-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="6a32f-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a32f-127">OUTPUTS</span></span>

### <span data-ttu-id="6a32f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6a32f-128">System.String</span></span>

## <span data-ttu-id="6a32f-129">Note</span><span class="sxs-lookup"><span data-stu-id="6a32f-129">NOTES</span></span>

## <span data-ttu-id="6a32f-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a32f-130">RELATED LINKS</span></span>

[<span data-ttu-id="6a32f-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="6a32f-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


