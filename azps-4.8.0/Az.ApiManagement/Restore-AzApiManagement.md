---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d99db4c9fe2c69e2177d9b35e15b49957e910014
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191705"
---
# <span data-ttu-id="0a943-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a943-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="0a943-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a943-102">SYNOPSIS</span></span>
<span data-ttu-id="0a943-103">Ripristina un servizio di gestione delle API dal BLOB di archiviazione di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="0a943-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="0a943-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a943-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a943-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a943-105">DESCRIPTION</span></span>
<span data-ttu-id="0a943-106">Il cmdlet **Restore-AzApiManagement** ripristina un servizio di gestione API dal backup specificato che risiede in un BLOB AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="0a943-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="0a943-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a943-107">EXAMPLES</span></span>

### <span data-ttu-id="0a943-108">Esempio 1: ripristinare un servizio di gestione delle API</span><span class="sxs-lookup"><span data-stu-id="0a943-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="0a943-109">Questo comando ripristina un servizio di gestione API da BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a943-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="0a943-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a943-110">PARAMETERS</span></span>

### <span data-ttu-id="0a943-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a943-111">-DefaultProfile</span></span>
<span data-ttu-id="0a943-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a943-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a943-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a943-113">-Name</span></span>
<span data-ttu-id="0a943-114">Specifica il nome dell'istanza di gestione API che verrà ripristinata con il backup.</span><span class="sxs-lookup"><span data-stu-id="0a943-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="0a943-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a943-115">-PassThru</span></span>
<span data-ttu-id="0a943-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="0a943-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0a943-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="0a943-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0a943-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a943-118">-ResourceGroupName</span></span>
<span data-ttu-id="0a943-119">Specifica il nome del gruppo di risorse in cui è presente la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="0a943-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="0a943-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="0a943-120">-SourceBlobName</span></span>
<span data-ttu-id="0a943-121">Specifica il nome del BLOB di origine del backup di Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="0a943-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="0a943-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="0a943-122">-SourceContainerName</span></span>
<span data-ttu-id="0a943-123">Specifica il nome del contenitore di origine del backup di Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="0a943-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="0a943-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="0a943-124">-StorageContext</span></span>
<span data-ttu-id="0a943-125">Specifica il contesto di connessione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0a943-125">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="0a943-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a943-126">CommonParameters</span></span>
<span data-ttu-id="0a943-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a943-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a943-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a943-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a943-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a943-129">INPUTS</span></span>

### <span data-ttu-id="0a943-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0a943-130">System.String</span></span>

## <span data-ttu-id="0a943-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a943-131">OUTPUTS</span></span>

### <span data-ttu-id="0a943-132">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a943-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="0a943-133">Note</span><span class="sxs-lookup"><span data-stu-id="0a943-133">NOTES</span></span>

## <span data-ttu-id="0a943-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a943-134">RELATED LINKS</span></span>

[<span data-ttu-id="0a943-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a943-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="0a943-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a943-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="0a943-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a943-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="0a943-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a943-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

