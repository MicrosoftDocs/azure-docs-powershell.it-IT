---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/restore-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 1fc22563949f44882d0b6ed1f864d217faacff9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519780"
---
# <span data-ttu-id="e5766-101">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5766-101">Restore-AzureRmApiManagement</span></span>

## <span data-ttu-id="e5766-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5766-102">SYNOPSIS</span></span>
<span data-ttu-id="e5766-103">Ripristina un servizio di gestione delle API dal BLOB di archiviazione di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="e5766-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5766-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5766-104">SYNTAX</span></span>

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5766-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5766-105">DESCRIPTION</span></span>
<span data-ttu-id="e5766-106">Il cmdlet **Restore-AzureRmApiManagement** ripristina un servizio di gestione API dal backup specificato che risiede in un BLOB AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="e5766-106">The **Restore-AzureRmApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="e5766-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5766-107">EXAMPLES</span></span>

### <span data-ttu-id="e5766-108">Esempio 1: ripristinare un servizio di gestione delle API</span><span class="sxs-lookup"><span data-stu-id="e5766-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="e5766-109">Questo comando ripristina un servizio di gestione API da BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5766-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="e5766-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5766-110">PARAMETERS</span></span>

### <span data-ttu-id="e5766-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5766-111">-DefaultProfile</span></span>
<span data-ttu-id="e5766-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5766-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5766-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5766-113">-Name</span></span>
<span data-ttu-id="e5766-114">Specifica il nome dell'istanza di gestione API che verrà ripristinata con il backup.</span><span class="sxs-lookup"><span data-stu-id="e5766-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5766-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5766-115">-PassThru</span></span>
<span data-ttu-id="e5766-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e5766-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e5766-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e5766-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5766-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5766-118">-ResourceGroupName</span></span>
<span data-ttu-id="e5766-119">Specifica il nome del gruppo di risorse in cui è presente la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="e5766-119">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5766-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="e5766-120">-SourceBlobName</span></span>
<span data-ttu-id="e5766-121">Specifica il nome del BLOB di origine del backup di Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e5766-121">Specifies the name of the Azure storage backup source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5766-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="e5766-122">-SourceContainerName</span></span>
<span data-ttu-id="e5766-123">Specifica il nome del contenitore di origine del backup di Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e5766-123">Specifies the name of the Azure storage backup source container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5766-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="e5766-124">-StorageContext</span></span>
<span data-ttu-id="e5766-125">Specifica il contesto di connessione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e5766-125">Specifies the storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5766-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5766-126">CommonParameters</span></span>
<span data-ttu-id="e5766-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5766-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5766-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5766-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5766-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5766-129">INPUTS</span></span>

### <span data-ttu-id="e5766-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e5766-130">System.String</span></span>

## <span data-ttu-id="e5766-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5766-131">OUTPUTS</span></span>

### <span data-ttu-id="e5766-132">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5766-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="e5766-133">Note</span><span class="sxs-lookup"><span data-stu-id="e5766-133">NOTES</span></span>

## <span data-ttu-id="e5766-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5766-134">RELATED LINKS</span></span>

[<span data-ttu-id="e5766-135">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5766-135">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="e5766-136">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5766-136">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="e5766-137">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5766-137">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="e5766-138">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5766-138">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)


