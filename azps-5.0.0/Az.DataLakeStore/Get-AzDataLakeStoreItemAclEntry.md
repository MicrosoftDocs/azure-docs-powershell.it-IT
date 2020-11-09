---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 02ff6856cf61664c1bd00e7d88fc7f8de999f2a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297948"
---
# <span data-ttu-id="ee1e1-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ee1e1-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="ee1e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee1e1-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1e1-103">Ottiene una voce nell'ACL di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ee1e1-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ee1e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee1e1-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee1e1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1e1-105">DESCRIPTION</span></span>
<span data-ttu-id="ee1e1-106">Il cmdlet **Get-AzDataLakeStoreItemAclEntry** ottiene una voce (ACE) nell'elenco di controllo di accesso (ACL) di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ee1e1-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ee1e1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee1e1-107">EXAMPLES</span></span>

### <span data-ttu-id="ee1e1-108">Esempio 1: ottenere l'ACL per una cartella</span><span class="sxs-lookup"><span data-stu-id="ee1e1-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="ee1e1-109">Questo comando consente di ottenere l'ACL per la directory radice dell'account di data Lake Store specificato</span><span class="sxs-lookup"><span data-stu-id="ee1e1-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="ee1e1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee1e1-110">PARAMETERS</span></span>

### <span data-ttu-id="ee1e1-111">-Account</span><span class="sxs-lookup"><span data-stu-id="ee1e1-111">-Account</span></span>
<span data-ttu-id="ee1e1-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ee1e1-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ee1e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1e1-113">-DefaultProfile</span></span>
<span data-ttu-id="ee1e1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee1e1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee1e1-115">-Path</span><span class="sxs-lookup"><span data-stu-id="ee1e1-115">-Path</span></span>
<span data-ttu-id="ee1e1-116">Specifica il percorso dello Store Data Lake dell'elemento per cui questo cmdlet ottiene una voce ACE, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="ee1e1-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ee1e1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1e1-117">CommonParameters</span></span>
<span data-ttu-id="ee1e1-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee1e1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1e1-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee1e1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1e1-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee1e1-120">INPUTS</span></span>

### <span data-ttu-id="ee1e1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ee1e1-121">System.String</span></span>

### <span data-ttu-id="ee1e1-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="ee1e1-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="ee1e1-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee1e1-123">OUTPUTS</span></span>

### <span data-ttu-id="ee1e1-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="ee1e1-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="ee1e1-125">Note</span><span class="sxs-lookup"><span data-stu-id="ee1e1-125">NOTES</span></span>

## <span data-ttu-id="ee1e1-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee1e1-126">RELATED LINKS</span></span>

[<span data-ttu-id="ee1e1-127">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ee1e1-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="ee1e1-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ee1e1-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


