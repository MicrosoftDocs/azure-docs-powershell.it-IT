---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: 576c623b942ec496d2800c1ad5432f72eb6911bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673663"
---
# <span data-ttu-id="c7489-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c7489-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="c7489-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7489-102">SYNOPSIS</span></span>
<span data-ttu-id="c7489-103">Eseguire il backup di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="c7489-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="c7489-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7489-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7489-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7489-105">DESCRIPTION</span></span>
<span data-ttu-id="c7489-106">Il cmdlet **backup-AzApiManagement** consente di eseguire un backup di un'istanza di un servizio di gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7489-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="c7489-107">Questo cmdlet archivia il backup come BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7489-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="c7489-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7489-108">EXAMPLES</span></span>

### <span data-ttu-id="c7489-109">Esempio 1: eseguire il backup di un servizio di gestione API</span><span class="sxs-lookup"><span data-stu-id="c7489-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="c7489-110">Questo comando consente di eseguire il backup di un servizio di gestione delle API in un BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c7489-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="c7489-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7489-111">PARAMETERS</span></span>

### <span data-ttu-id="c7489-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7489-112">-DefaultProfile</span></span>
<span data-ttu-id="c7489-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7489-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7489-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7489-114">-Name</span></span>
<span data-ttu-id="c7489-115">Specifica il nome della distribuzione di gestione delle API di cui è stato eseguito il backup di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7489-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="c7489-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7489-116">-PassThru</span></span>
<span data-ttu-id="c7489-117">Indica che questo cmdlet restituisce l'oggetto **PsApiManagement** di cui è stato eseguito il backup, se l'operazione viene eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="c7489-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="c7489-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7489-118">-ResourceGroupName</span></span>
<span data-ttu-id="c7489-119">Specifica il nome del gruppo di risorse in cui è presente la distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="c7489-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="c7489-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="c7489-120">-StorageContext</span></span>
<span data-ttu-id="c7489-121">Specifica un contesto di connessione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c7489-121">Specifies a storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7489-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="c7489-122">-TargetBlobName</span></span>
<span data-ttu-id="c7489-123">Specifica il nome del BLOB per il backup.</span><span class="sxs-lookup"><span data-stu-id="c7489-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="c7489-124">Se il BLOB non esiste, questo cmdlet lo crea.</span><span class="sxs-lookup"><span data-stu-id="c7489-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="c7489-125">Questo cmdlet genera un valore predefinito basato sul modello seguente: {Name}-{yyyy-MM-DD-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="c7489-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7489-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="c7489-126">-TargetContainerName</span></span>
<span data-ttu-id="c7489-127">Specifica il nome del contenitore del BLOB per il backup.</span><span class="sxs-lookup"><span data-stu-id="c7489-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="c7489-128">Se il contenitore non esiste, questo cmdlet lo crea.</span><span class="sxs-lookup"><span data-stu-id="c7489-128">If the container does not exist, this cmdlet creates it.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7489-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7489-129">CommonParameters</span></span>
<span data-ttu-id="c7489-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7489-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7489-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7489-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7489-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7489-132">INPUTS</span></span>

### <span data-ttu-id="c7489-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c7489-133">System.String</span></span>

### <span data-ttu-id="c7489-134">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c7489-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c7489-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7489-135">OUTPUTS</span></span>

### <span data-ttu-id="c7489-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c7489-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c7489-137">Note</span><span class="sxs-lookup"><span data-stu-id="c7489-137">NOTES</span></span>

## <span data-ttu-id="c7489-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7489-138">RELATED LINKS</span></span>

[<span data-ttu-id="c7489-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c7489-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="c7489-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c7489-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="c7489-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c7489-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="c7489-142">Ripristinare-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c7489-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)

