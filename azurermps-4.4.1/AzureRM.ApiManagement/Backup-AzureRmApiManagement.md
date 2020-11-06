---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: d036b31f521736420b91b04b4f6f5513f3dbc50d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519653"
---
# <span data-ttu-id="ece55-101">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ece55-101">Backup-AzureRmApiManagement</span></span>

## <span data-ttu-id="ece55-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ece55-102">SYNOPSIS</span></span>
<span data-ttu-id="ece55-103">Eseguire il backup di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="ece55-103">Backs up an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ece55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ece55-104">SYNTAX</span></span>

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ece55-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece55-105">DESCRIPTION</span></span>
<span data-ttu-id="ece55-106">Il cmdlet **backup-AzureRmApiManagement** consente di eseguire un backup di un'istanza di un servizio di gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="ece55-106">The **Backup-AzureRmApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="ece55-107">Questo cmdlet archivia il backup come BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ece55-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="ece55-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ece55-108">EXAMPLES</span></span>

### <span data-ttu-id="ece55-109">Esempio 1: eseguire il backup di un servizio di gestione API</span><span class="sxs-lookup"><span data-stu-id="ece55-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="ece55-110">Questo comando consente di eseguire il backup di un servizio di gestione delle API in un BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ece55-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="ece55-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ece55-111">PARAMETERS</span></span>

### <span data-ttu-id="ece55-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="ece55-112">-Name</span></span>
<span data-ttu-id="ece55-113">Specifica il nome della distribuzione di gestione delle API di cui è stato eseguito il backup di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ece55-113">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="ece55-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ece55-114">-PassThru</span></span>
<span data-ttu-id="ece55-115">Indica che questo cmdlet restituisce l'oggetto **PsApiManagement** di cui è stato eseguito il backup, se l'operazione viene eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="ece55-115">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="ece55-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece55-116">-ResourceGroupName</span></span>
<span data-ttu-id="ece55-117">Specifica il nome del gruppo di risorse in cui è presente la distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="ece55-117">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="ece55-118">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="ece55-118">-StorageContext</span></span>
<span data-ttu-id="ece55-119">Specifica un contesto di connessione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ece55-119">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="ece55-120">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="ece55-120">-TargetBlobName</span></span>
<span data-ttu-id="ece55-121">Specifica il nome del BLOB per il backup.</span><span class="sxs-lookup"><span data-stu-id="ece55-121">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="ece55-122">Se il BLOB non esiste, questo cmdlet lo crea.</span><span class="sxs-lookup"><span data-stu-id="ece55-122">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="ece55-123">Questo cmdlet genera un valore predefinito basato sul modello seguente:</span><span class="sxs-lookup"><span data-stu-id="ece55-123">This cmdlet generates a default value based on the following pattern:</span></span> 

<span data-ttu-id="ece55-124">{Nome}-{aaaa-MM-DD-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="ece55-124">{Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="ece55-125">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="ece55-125">-TargetContainerName</span></span>
<span data-ttu-id="ece55-126">Specifica il nome del contenitore del BLOB per il backup.</span><span class="sxs-lookup"><span data-stu-id="ece55-126">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="ece55-127">Se il contenitore non esiste, questo cmdlet lo crea.</span><span class="sxs-lookup"><span data-stu-id="ece55-127">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="ece55-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece55-128">-DefaultProfile</span></span>
<span data-ttu-id="ece55-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ece55-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ece55-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece55-130">CommonParameters</span></span>
<span data-ttu-id="ece55-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece55-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece55-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece55-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece55-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ece55-133">INPUTS</span></span>

## <span data-ttu-id="ece55-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ece55-134">OUTPUTS</span></span>

### <span data-ttu-id="ece55-135">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ece55-135">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ece55-136">Note</span><span class="sxs-lookup"><span data-stu-id="ece55-136">NOTES</span></span>

## <span data-ttu-id="ece55-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ece55-137">RELATED LINKS</span></span>

[<span data-ttu-id="ece55-138">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ece55-138">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="ece55-139">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ece55-139">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="ece55-140">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ece55-140">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="ece55-141">Ripristinare-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ece55-141">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


