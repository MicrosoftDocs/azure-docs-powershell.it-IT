---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d1c7e1938d50e4a970dbec15568bc5cf10257639
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007389"
---
# <span data-ttu-id="fbc62-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="fbc62-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="fbc62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbc62-102">SYNOPSIS</span></span>
<span data-ttu-id="fbc62-103">Ripristina un servizio di gestione API dal BLOB di archiviazione di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="fbc62-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="fbc62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbc62-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbc62-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fbc62-105">DESCRIPTION</span></span>
<span data-ttu-id="fbc62-106">Il cmdlet **Restore-AzApiManagement** ripristina un servizio di gestione API dal backup specificato che risiede in un BLOB Azurestorage.</span><span class="sxs-lookup"><span data-stu-id="fbc62-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="fbc62-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbc62-107">EXAMPLES</span></span>

### <span data-ttu-id="fbc62-108">Esempio 1: Ripristinare un servizio di gestione delle API</span><span class="sxs-lookup"><span data-stu-id="fbc62-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="fbc62-109">Questo comando ripristina un servizio di gestione API dal BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fbc62-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="fbc62-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbc62-110">PARAMETERS</span></span>

### <span data-ttu-id="fbc62-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbc62-111">-DefaultProfile</span></span>
<span data-ttu-id="fbc62-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbc62-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbc62-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fbc62-113">-Name</span></span>
<span data-ttu-id="fbc62-114">Specifica il nome dell'istanza di Gestione API che verrà ripristinata con il backup.</span><span class="sxs-lookup"><span data-stu-id="fbc62-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="fbc62-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbc62-115">-PassThru</span></span>
<span data-ttu-id="fbc62-116">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="fbc62-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fbc62-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="fbc62-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fbc62-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbc62-118">-ResourceGroupName</span></span>
<span data-ttu-id="fbc62-119">Specifica il nome del gruppo di risorse in cui esiste Gestione API.</span><span class="sxs-lookup"><span data-stu-id="fbc62-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="fbc62-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="fbc62-120">-SourceBlobName</span></span>
<span data-ttu-id="fbc62-121">Specifica il nome del BLOB di origine del backup di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fbc62-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="fbc62-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="fbc62-122">-SourceContainerName</span></span>
<span data-ttu-id="fbc62-123">Specifica il nome del contenitore di origine del backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="fbc62-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="fbc62-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="fbc62-124">-StorageContext</span></span>
<span data-ttu-id="fbc62-125">Specifica il contesto della connessione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fbc62-125">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="fbc62-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbc62-126">CommonParameters</span></span>
<span data-ttu-id="fbc62-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbc62-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbc62-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fbc62-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbc62-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="fbc62-129">INPUTS</span></span>

### <span data-ttu-id="fbc62-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fbc62-130">System.String</span></span>

## <span data-ttu-id="fbc62-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbc62-131">OUTPUTS</span></span>

### <span data-ttu-id="fbc62-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="fbc62-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="fbc62-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="fbc62-133">NOTES</span></span>

## <span data-ttu-id="fbc62-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbc62-134">RELATED LINKS</span></span>

[<span data-ttu-id="fbc62-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="fbc62-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="fbc62-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="fbc62-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="fbc62-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="fbc62-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="fbc62-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="fbc62-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


