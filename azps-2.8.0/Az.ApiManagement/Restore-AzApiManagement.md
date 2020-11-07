---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: aa9049489b5a4c28015c208998dae535f514e8f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675919"
---
# <span data-ttu-id="eb635-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb635-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="eb635-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb635-102">SYNOPSIS</span></span>
<span data-ttu-id="eb635-103">Ripristina un servizio di gestione delle API dal BLOB di archiviazione di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="eb635-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="eb635-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb635-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb635-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb635-105">DESCRIPTION</span></span>
<span data-ttu-id="eb635-106">Il cmdlet **Restore-AzApiManagement** ripristina un servizio di gestione API dal backup specificato che risiede in un BLOB AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="eb635-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="eb635-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb635-107">EXAMPLES</span></span>

### <span data-ttu-id="eb635-108">Esempio 1: ripristinare un servizio di gestione delle API</span><span class="sxs-lookup"><span data-stu-id="eb635-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="eb635-109">Questo comando ripristina un servizio di gestione API da BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="eb635-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="eb635-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb635-110">PARAMETERS</span></span>

### <span data-ttu-id="eb635-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb635-111">-DefaultProfile</span></span>
<span data-ttu-id="eb635-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb635-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb635-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb635-113">-Name</span></span>
<span data-ttu-id="eb635-114">Specifica il nome dell'istanza di gestione API che verrà ripristinata con il backup.</span><span class="sxs-lookup"><span data-stu-id="eb635-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="eb635-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb635-115">-PassThru</span></span>
<span data-ttu-id="eb635-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="eb635-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="eb635-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="eb635-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eb635-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb635-118">-ResourceGroupName</span></span>
<span data-ttu-id="eb635-119">Specifica il nome del gruppo di risorse in cui è presente la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="eb635-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="eb635-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="eb635-120">-SourceBlobName</span></span>
<span data-ttu-id="eb635-121">Specifica il nome del BLOB di origine del backup di Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="eb635-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="eb635-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="eb635-122">-SourceContainerName</span></span>
<span data-ttu-id="eb635-123">Specifica il nome del contenitore di origine del backup di Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="eb635-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="eb635-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="eb635-124">-StorageContext</span></span>
<span data-ttu-id="eb635-125">Specifica il contesto di connessione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eb635-125">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="eb635-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb635-126">CommonParameters</span></span>
<span data-ttu-id="eb635-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb635-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb635-128">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb635-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb635-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb635-129">INPUTS</span></span>

### <span data-ttu-id="eb635-130">System. String</span><span class="sxs-lookup"><span data-stu-id="eb635-130">System.String</span></span>

## <span data-ttu-id="eb635-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb635-131">OUTPUTS</span></span>

### <span data-ttu-id="eb635-132">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb635-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="eb635-133">Note</span><span class="sxs-lookup"><span data-stu-id="eb635-133">NOTES</span></span>

## <span data-ttu-id="eb635-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb635-134">RELATED LINKS</span></span>

[<span data-ttu-id="eb635-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb635-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="eb635-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb635-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="eb635-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb635-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="eb635-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb635-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


