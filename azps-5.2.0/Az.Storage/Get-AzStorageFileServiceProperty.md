---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 0824045a6b916d34a7b268c32e9667e954a4e1e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324976"
---
# <span data-ttu-id="3c044-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3c044-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="3c044-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c044-102">SYNOPSIS</span></span>
<span data-ttu-id="3c044-103">Ottiene le proprietà del servizio per i servizi file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3c044-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="3c044-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c044-104">SYNTAX</span></span>

### <span data-ttu-id="3c044-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c044-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c044-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="3c044-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c044-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="3c044-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c044-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c044-108">DESCRIPTION</span></span>
<span data-ttu-id="3c044-109">Il cmdlet **Get-AzStorageFileServiceProperty** ottiene le proprietà del servizio per i servizi file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3c044-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="3c044-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c044-110">EXAMPLES</span></span>

### <span data-ttu-id="3c044-111">Esempio 1: ottenere la proprietà Servizi file di archiviazione di Azure di un account di archiviazione specificato</span><span class="sxs-lookup"><span data-stu-id="3c044-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="3c044-112">Questo comando ottiene la proprietà Servizi file di un account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="3c044-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="3c044-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c044-113">PARAMETERS</span></span>

### <span data-ttu-id="3c044-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c044-114">-DefaultProfile</span></span>
<span data-ttu-id="3c044-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c044-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c044-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c044-116">-ResourceGroupName</span></span>
<span data-ttu-id="3c044-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3c044-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c044-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c044-118">-ResourceId</span></span>
<span data-ttu-id="3c044-119">Immettere un ID risorsa dell'account di archiviazione o un ID risorsa delle proprietà del servizio file.</span><span class="sxs-lookup"><span data-stu-id="3c044-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c044-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3c044-120">-StorageAccount</span></span>
<span data-ttu-id="3c044-121">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3c044-121">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c044-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3c044-122">-StorageAccountName</span></span>
<span data-ttu-id="3c044-123">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3c044-123">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c044-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c044-124">CommonParameters</span></span>
<span data-ttu-id="3c044-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c044-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c044-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c044-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c044-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c044-127">INPUTS</span></span>

### <span data-ttu-id="3c044-128">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3c044-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="3c044-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3c044-129">System.String</span></span>

## <span data-ttu-id="3c044-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c044-130">OUTPUTS</span></span>

### <span data-ttu-id="3c044-131">Microsoft. Azure. Commands. Management. storage. Models. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="3c044-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="3c044-132">Note</span><span class="sxs-lookup"><span data-stu-id="3c044-132">NOTES</span></span>

## <span data-ttu-id="3c044-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c044-133">RELATED LINKS</span></span>
