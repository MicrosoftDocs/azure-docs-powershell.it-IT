---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 8473cc65ec6afffb9433159d848d9e7b8629a351
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518712"
---
# <span data-ttu-id="0a8fe-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a8fe-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="0a8fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a8fe-102">SYNOPSIS</span></span>
<span data-ttu-id="0a8fe-103">Ottiene una voce nell'ACL di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0a8fe-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a8fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a8fe-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a8fe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a8fe-105">DESCRIPTION</span></span>
<span data-ttu-id="0a8fe-106">Il cmdlet **Get-AzureRmDataLakeStoreItemAclEntry** ottiene una voce (ACE) nell'elenco di controllo di accesso (ACL) di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0a8fe-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0a8fe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a8fe-107">EXAMPLES</span></span>

### <span data-ttu-id="0a8fe-108">Esempio 1: ottenere l'ACL per una cartella</span><span class="sxs-lookup"><span data-stu-id="0a8fe-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="0a8fe-109">Questo comando consente di ottenere l'ACL per la directory radice dell'account di data Lake Store specificato</span><span class="sxs-lookup"><span data-stu-id="0a8fe-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="0a8fe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a8fe-110">PARAMETERS</span></span>

### <span data-ttu-id="0a8fe-111">-Account</span><span class="sxs-lookup"><span data-stu-id="0a8fe-111">-Account</span></span>
<span data-ttu-id="0a8fe-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0a8fe-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0a8fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a8fe-113">-DefaultProfile</span></span>
<span data-ttu-id="0a8fe-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a8fe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a8fe-115">-Path</span><span class="sxs-lookup"><span data-stu-id="0a8fe-115">-Path</span></span>
<span data-ttu-id="0a8fe-116">Specifica il percorso dello Store Data Lake dell'elemento per cui questo cmdlet ottiene una voce ACE, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="0a8fe-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0a8fe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a8fe-117">CommonParameters</span></span>
<span data-ttu-id="0a8fe-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a8fe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a8fe-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a8fe-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a8fe-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a8fe-120">INPUTS</span></span>

### <span data-ttu-id="0a8fe-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0a8fe-121">System.String</span></span>

### <span data-ttu-id="0a8fe-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0a8fe-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="0a8fe-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a8fe-123">OUTPUTS</span></span>

### <span data-ttu-id="0a8fe-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="0a8fe-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="0a8fe-125">Note</span><span class="sxs-lookup"><span data-stu-id="0a8fe-125">NOTES</span></span>

## <span data-ttu-id="0a8fe-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a8fe-126">RELATED LINKS</span></span>

[<span data-ttu-id="0a8fe-127">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a8fe-127">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="0a8fe-128">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a8fe-128">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


