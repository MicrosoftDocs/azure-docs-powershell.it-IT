---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 9e19d8e205010ce55886761d2cbb7fd904d5277d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685538"
---
# <span data-ttu-id="e3fb6-101">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3fb6-101">Restore-AzureRmApiManagement</span></span>

## <span data-ttu-id="e3fb6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="e3fb6-103">Ripristina un servizio di gestione delle API dal BLOB di archiviazione di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="e3fb6-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3fb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3fb6-104">SYNTAX</span></span>

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3fb6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3fb6-105">DESCRIPTION</span></span>
<span data-ttu-id="e3fb6-106">Il cmdlet **Restore-AzureRmApiManagement** ripristina un servizio di gestione API dal backup specificato che risiede in un BLOB AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="e3fb6-106">The **Restore-AzureRmApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="e3fb6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3fb6-107">EXAMPLES</span></span>

### <span data-ttu-id="e3fb6-108">Esempio 1: ripristinare un servizio di gestione delle API</span><span class="sxs-lookup"><span data-stu-id="e3fb6-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="e3fb6-109">Questo comando ripristina un servizio di gestione API da BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3fb6-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="e3fb6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3fb6-110">PARAMETERS</span></span>

### <span data-ttu-id="e3fb6-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3fb6-111">-Name</span></span>
<span data-ttu-id="e3fb6-112">Specifica il nome dell'istanza di gestione API che verrà ripristinata con il backup.</span><span class="sxs-lookup"><span data-stu-id="e3fb6-112">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="e3fb6-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3fb6-113">-PassThru</span></span>
<span data-ttu-id="e3fb6-114">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e3fb6-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e3fb6-115">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e3fb6-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e3fb6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3fb6-116">-ResourceGroupName</span></span>
<span data-ttu-id="e3fb6-117">Specifica il nome del gruppo di risorse in cui è presente la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="e3fb6-117">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="e3fb6-118">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="e3fb6-118">-SourceBlobName</span></span>
<span data-ttu-id="e3fb6-119">Specifica il nome del BLOB di origine del backup di Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e3fb6-119">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="e3fb6-120">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="e3fb6-120">-SourceContainerName</span></span>
<span data-ttu-id="e3fb6-121">Specifica il nome del contenitore di origine del backup di Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e3fb6-121">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="e3fb6-122">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="e3fb6-122">-StorageContext</span></span>
<span data-ttu-id="e3fb6-123">Specifica il contesto di connessione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e3fb6-123">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="e3fb6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3fb6-124">-DefaultProfile</span></span>
<span data-ttu-id="e3fb6-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3fb6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3fb6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3fb6-126">CommonParameters</span></span>
<span data-ttu-id="e3fb6-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3fb6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3fb6-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3fb6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3fb6-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3fb6-129">INPUTS</span></span>

## <span data-ttu-id="e3fb6-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3fb6-130">OUTPUTS</span></span>

### <span data-ttu-id="e3fb6-131">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3fb6-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="e3fb6-132">Note</span><span class="sxs-lookup"><span data-stu-id="e3fb6-132">NOTES</span></span>

## <span data-ttu-id="e3fb6-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3fb6-133">RELATED LINKS</span></span>

[<span data-ttu-id="e3fb6-134">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3fb6-134">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="e3fb6-135">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3fb6-135">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="e3fb6-136">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3fb6-136">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="e3fb6-137">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3fb6-137">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)


